# AWS
1. a powerful web platform that provides 175 features to users
2. AWS developer tools: 
   1.  Web Console
   2.  Command Line Tool
   3.  IDE
   4.  SDK
   5.  Infra as Code: define cloud infra using familiar language
3.  Five Pillars  
    1.  Security
    2.  Performance Efficiency
    3.  Reliability
    4.  Operational Excellence
    5.  Cost Optimization
4.  Security  
    1.  focus on how to secure your infra on cloud
    2.  Both AWS and customer are responsible for the security on the cloud, AWS takes care of physical infra, software and networking capabilities of AWS services
    3.  For security, should adopt the model of **Zero Trust**
    4.  Think of security in terms of **Zero Trust** we need to apply security to all levels of our system  
        1.  Identity and Accesss Management aka. IAM  
            1.  managed by a service called IAM, use IAM policy to achieve Security   
                1.  The **Principal** specifies **WHO** permissions are given to
                2.  The **Action** specifies **WHAT** is being performed
                3.  THe **Resource** specifies **WHICH** properties are being accessed
            2.  every agent should have the **minimal permission necessary** to accomplish their functionality
        2.  Network Security  
            1.  Network Level Security  
            2.  Resource Level Security  
        3.  Data Encryption  
            1.  encrypting data anywhere, including in transit and at rest
            2.  All storage and DB services on AWS provide encryption by default
    5.  Performance Efficiency  
        1.  focus on how you can run services efficiently and scalably on cloud
        2.  Mental Model: think of your services as **cattle, not pets**
        3.  no single server should be essential for the operation of the service
        4.  Selection  
            1.  ability to choose the service that most closely to your workload
            2.  typical workload usually requires selection across four main category:   
                1.  Compute
                2.  Storage
                3.  Database
                4.  Network
        5.  Scalling  
            1.  vertical scalling
            2.  horizontal scalling
    6. Reliability
       1. how you can build service that is resilient to both service and infra disruption
       2. useful to think in terms of **Blast Raidus**, minimize the the blast radius of any individual component
       3. 