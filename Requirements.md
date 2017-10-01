## List of Definitions
**User:** User is any person accessing Eureka application from web or mobile.

**Authenticated User:** An authenticated user is a user who is logged in to the application.

**Annotation:** Annotation is web annotation; associations between two web resources, a set of connected resources including a body and target and conveys that the body is related to the target. ([Web Annotation Data Model](https://www.w3.org/TR/annotation-model/))

**Living History Item:** Posts created by users; including location, time and story. Living history stories may refer to tangible things or not. Stories are often related to a given time, people and location.

## Functional Requirements
### 1. Account Management
a. Users shall create their accounts after they provide their username, email and password.

b. Users shall be able to login using username and password.

c. Users shall be able to reset their password by using their email address.

d. Users shall have a profile page, which shows their activities.

### 2. Living History Items
#### Creation
a. Only authenticated (logged-in) users shall be able to create living history items.

b. Users shall provide at least a picture and a title when creating a living history item.

c. Users may provide additional information, such as location, time, sound or video.

	a. Location can be in formats such as, name, region, point-in-map or area-in-map.

	b. Time can be in formats such as, date, date-range, age, age-range.

d. Living History Items can be created using Web-interface or Mobile application.

	a. Mobile application users shall be able to can take a photo or choose a photo.

	b. Web interface users shall be able to upload a photo.
                                         
#### Editing
e. Users shall be able to edit their living history items as long as there's no annotation.

#### Display
f. Living history page shall display living history content, the author, and the annotations.

	a. Picture annotations shall be shown with indication to annotated region or point.

	b. Text annotations shall be shown with highlighting the text area.

	c. Video and sound annotations shall be shown pointing to the sound or video player.

g. Annotations shall be shown when highlights are hovered, in a pop-up view.

	a. A more button in this pop-up shall show next annotation if another annotation with same target exist.
h. Anonymous users shall display the public history items, but they cannot modify the content. 
### 3. Annotations
(WIP)

### 4. Site-features
i. The site should be compatible with all modern browsers.            
(WIP)

## Non-functional Requirements

1. System shall provide local content provider and an annotation store, seperately.
2. System shall have annotations targetted towards living history items content which 
is stored in local content provider.
3. System shall be scalable to multiple users.
4. System shall have responsive user-interface.
5. System shall consist of a web application and a mobile application.
6. System shall implement W3C's Web Annotation Model and a standard annotation storage strategy
for annotations.
7. The work shall adhere to third-party license requirements.
8. The work shall be provided with MIT open-source software license to open public.                          
             
