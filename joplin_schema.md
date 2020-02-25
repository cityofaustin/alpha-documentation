*last revised, Feb 25, 2020*

#Schema

**Following Pages inherit from Janis Base Page**

## Service Page 
  - Title
  - Short description
  - Topics [**ForeignKey: TopicPage**]
  - related departments [**ForeignKey: DepartmentPage**]
    - *Janis "contextual nav: offered by"*
  - steps
  - steps with locations [**can link to LocationPage**]
  - steps with options
  - dynamic [**can link to map snippets**]
    - *Janis "HTMLFromAdmin", map block, trashy, recollect*
  - contacts [**ForeignKey:Contact Snippet**]
  - additional content


## Information Page
  - Title
  - Topics [**ForeignKey: TopicPage**]
  - related departments [**ForeignKey: DepartmentPage**]
    - *Janis "contextual nav: offered by"*
  - description
  - additional content
  - contacts [**ForeignKey:Contact Snippet**]

## Department Page
  - Title
  - what we do
  - image [**ForeignKey: translatedImage**]
  - mission
  - contacts [**ForeignKey:Contact Snippet**]
  - department directors
    - name
    - title
    - photo (TranslatedImage)
    - about
  - job listings
  - top pages [**ForeignKey: InformationPage, ServicePage, GuidePage, OfficialDocumentPage**]
  - related pages [**ForeignKey: InformationPage, ServicePage, GuidePage, OfficialDocumentPage**]
                                                    
## Topic Collection Page
  - Title
  - Description
  - Theme [**ForeignKey: Theme**]
  - image [**ForeignKey: translatedImage**]
  - Topic Collection                                  
                                                    
## Topic Page
  - Title
  - Description
  - image [**ForeignKey: translatedImage**]
  - topic collections [**ForeignKey: TopicCollection**]
  - top pages [**ForeignKey: InformationPage, ServicePage, GuidePage, OfficialDocumentPage**]
                                                    
## Official Document Page
  - Title
  - Description 
  - topics [**ForeignKey TopicPage**]
  - related departments [**ForeignKey: DepartmentPage**]
    - *Janis "contextual nav: offered by" *
  - official document
    - page (Parental Key, official document page)
    - date
    - title
    - authoring_office
    - summary
    - name
    - document [**ForeignKey: Document**]

## Guide Page
  - Title
  - Description
  - topics [**ForeignKey TopicPage**]
  - related departments [**ForeignKey: DepartmentPage**]
    - *Janis "contextual nav: offered by" *
  - image [**ForeignKey: translatedImage**]
  - sections [**can include InformationPage, ServicePage, but no ForeignKey**]
  - contacts [**ForeignKey:Contact Snippet**]

## Form Container
  - Title
  - Description
  - topics [**ForeignKey TopicPage**]
  - related departments
    - *Janis "contextual nav: offered by" *
  - form url
    - renders the form in an iframe, see `alpha-formstack-theme` repo

## Location Page
  - Title
  - Location Physical Address
    - physical_street
    - physical_unit
    - physical_city
    - physical_state
    _ physical_zip
  - Image [**ForeignKey: translatedImage**]
  - Location Mailing Address
    - mailing street
    - mailing city
    - mailing state
    - mailing zip
  - Alternate Name
  - Contact Info
    - phone number
    - phone description
    - email
  - Location Details
    - nearest bus 1
    - nearest bus 2
    - nearest bus 3
  - Related Services [**ForeignKey: service Page**]
  - hours exceptions

## Event Page
  - Title
  - Description
  - date
  - Event time
    - start time
    - end time
  - Location Blocks
    - city location
      - location page (PageChooser Location Page)
      - additional details
    - remote location
      - name
      - street
      - unit
      - city
      - state
      - zip
      - additional details
  - event is free
  - fees
    - fee
    - fee label
  - registration url
  - related departments [**Foreign Key: department page**]
  - contact [**Foreign Key: contact**]
  - canceled

The following do not inherit from Janis Base Page

## Theme

## Translated Image
  - Title                                               

## Three One One                                                   
                                                    
## Contact
  - name 
  - email
  - phone number
  - location (snippet)
  - locationPage
  - hours
  - hours exception
  - social media

## Phone Number
  - number 
  - description

## Location
  **deprecated**
  - name
  - street
  - city
  - state zip country

## Contact Day and Duration
  - day and duration                                                
                                                    
                                                    
