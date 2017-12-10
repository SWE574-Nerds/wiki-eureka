**Feature**: Eureka login      
  I want to use this template for my feature file     

  **Scenario Outline**: Eureka login with valid credentials     
    **Given** I am on Eureka Website   
    **When** Already have an account     
    **And** I enter username as "<username>"     
    **And** enter password as "<password>"     
    **And** click login button     
    **Then** I should be able to login successfully and see "<username>"        
    **Then** I click logout      

    Examples:
      | username                 | password               |
      | AutomatedTestUser        | AutomatedTestPassword  |
      | AutomatedTestUser        | AutomatedTestPassword  |


  **Scenario Outline**: Eureka login with invalid credentials     
    **Given** I am on Eureka Website    
    **When** Already have an account    
    **And** I enter username as "<username>"    
    **And** enter password as "<password>"    
    **And** click login button    
    **Then** I should NOT be able to login successfully     

    Examples:
      | username                 | password    |
      | botAccess1               | botAccess1  |
      | botAccess2               | botAccess2  |


**Feature:** Listory tests
  I want to use this template for my feature file    

  **Scenario Outline**: List history items   
    **Given** I am on Eureka Website    
    **When** I login with valid credentials using "<username>" and "<password>"    
    **And** I click to see history items list    
    **Then** I should be able to list the history items    
    **Then** I click logout    

    Examples:
      | username                 | password               |
      | AutomatedTestUser        | AutomatedTestPassword  |  