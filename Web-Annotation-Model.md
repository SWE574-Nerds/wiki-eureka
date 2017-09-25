# Web Annotation Model

## Summary

Web annotations, put simply, are associations between two web resource. By providing an 
annotation for a resource, a connection is made, to another resource that may or may
not be host at the same host with the annotated resource. With these annotations users
can find relative resources by looking at annotations over the other.

Web Annotation Model is a standardized and very generalized way of storing annotations.
These storage method is specialised to be portable, and very extendable (meaning any
web resource can be either annotated or be an annotation). The storage systems that 
support this model also tend not to suffer from performance losses as they're specialized
to deal with complex graphs and huge datasets.

This model, however, does not provide the resources. These models really are "annotations"
in basic sense, It's user's or developers responsibility to provide access to these web 
resources.

The standard definition can be found here :https://www.w3.org/TR/annotation-model/ 

![](https://github.com/SWE574-Groupago/heritago/wiki/images/research/webAnnotationModel.png)

Above is a very simple graph that shows the generic structure of an annotation.

These different nodes, are as stated in the definition, are nodes in a graph and simply 
are linked to each other. 

## Data structure

To conform with the annotation model documentation, We'll be using JSON-LD in this section. We'll be covering
the data types under RDF section.

```json
{
  "@context": "http://www.w3.org/ns/anno.jsonld",
  "id": "http://example.org/anno1",
  "type": "Annotation",
  "body": "http://example.org/post1",
  "target": "http://example.com/page1"
}
```

This is a sample annotation data but it shows most of the characteristics of Web annotation model.
It has an id for easy reference,
It has a type.
It has a body and target.
@context is to indicate in which context this annotation is relevant.

What's needed to be said about this is, any information you see here is actually a single independent row in a database. By looking at this example It may be looking a simple as storing in a DB like redis because It's JSON. 

But the reality is that It's just the definition of the data. You can export this from a storage unit as this, or import it back, but that's not how it's being stored or processed by the data management system. If we look at how that's processed in a DBMS that supports these:

<img src="https://github.com/SWE574-Nerds/friendly-eureka/raw/master/images/triplestored_annotation.png" width="800px">

And the graph will look like this
<img src="https://github.com/SWE574-Nerds/friendly-eureka/raw/master/images/triplestored_annotation_2.png" width="400px">

As you can see, each field in the given JSON is actually a relation. This is a very good case because this means there's a lot of flexibility when it comes to modifying, adding new annotations. Or simply re-using previously created annotations etc.

This annotation storage model is called Triplestore. Web Annotation Model is ideally used with triplestores as there are pretty standardized triplestores that handle this data structure.

## RDF

As previously mentioned, The data is in fact, NOT Json. It is merely a representation in the documentation just to provide an easy to understand set of examples. This particular format is called JSON-LD and it's supported by many RDF storages when it comes to exporting and importing data.

The Resource Description Framework (RDF) ıs a way of describing web resources at metadata, designed by of World Wide Web Consortium (W3C). RDF data may come in many forms, some of these types are:

1. RDFa
2. Pretty RDF
3. RDF/XML
4. N3
5. N-Triples
6. JSON-LD

and so on. In this document, We'll stick with RDF/XML and JSON-LD as these are the most common formats widely used and supported, plus everyone is familiar with XML and JSON.

The DBMSs used to store annotations are not specialized to store annotations, they're specialized to store RDF data and Web Annotation Model is just a subset of RDF representation, providing a structure of how RDF data should be structured, linking against one another. You can think of Web Annotation Models are what DB Schemas are for Relational databases, to graph databases. 

If we were to rewrite the prevoiusly provided sample.json in RDF/XML it would look like this: 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<rdf:RDF
   xmlns:oa="http://www.w3.org/ns/oa#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
>
  <rdf:Description rdf:about="http://example.org/anno1">
    <rdf:type rdf:resource="file:///base/data/home/apps/s%7Erdf-translator/1.380697414950152317/Annotation"/>
    <oa:hasBody rdf:resource="http://example.org/post1"/>
    <oa:hasTarget rdf:resource="http://example.com/page1"/>
  </rdf:Description>
</rdf:RDF>
```

## Technologies

It's very convenient to use a pre-existent technology to store RDF data. There are a lot of options to choose:
1. Neo4J/RDF
2. Sesame
3. Jena TDB 
4. OpenRDF
5. Ontotext
6. Systap
7. Stardog

And for communicating with these services: 
1. Sparql
2. Apache JENA
3. REST (If DBMS provides one)

## Resources
1. Difference between Triplestore and Graph DB : https://neo4j.com/blog/rdf-triple-store-vs-labeled-property-graph-difference/
2. Nice RDF storage data examples : https://github.com/jbarrasa/explicitsemanticsneo4j/blob/master/moviesontology.owl
3. Using RDF to Annotate the (Semantic) Web, Cross P., Miller L., Palmer S.  http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.68.1566&rep=rep1&type=pdf
4. RDF Data conversion utility :http://rdf-translator.appspot.com

