# Technology Stack

## Back End
* Ubuntu Linux OS
* Apache HTTP server configured as reverse proxy
* JRE 8
* Apache Tomcat Java application server
* Web service application, incorporating:
   * Data model
        * Embedded Apache Derby database
        * Hibernate ORM
        * Custom entity classes
        * Spring Boot Data
        * Custom data repository interfaces
* Service controllers
    * Spring MVC
    * Custom controller classes
* View composition & serialization
    * Jackson JSON
    * Custom view classes & interfaces
* Authentication
    * Spring Security
    * Google Sign In (external service; see https://developers.google.com/identity)
    * Custom authentication verification class
    
## Front end
* Android OS
* Data model
    * Custom entity and other model classes
    * Custom type converters
* Remote service interfaces
    * Retrofit
    * ReactiveX
    * Gson
* View Model components
    * Android Lifecycle framework (ViewModel & LiveData)
    * Custom view model classes
* View
    * Custom ViewPager and ViewPager.Adapter classes
    * Custom layouts
* Controller
    * Custom activity and fragment classes
* Authentication
    * Google Sign In (external service; see https://developers.google.com/identity)
 