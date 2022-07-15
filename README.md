# Microservices_v1
First version of Multiplication Microservice

So far we just have a basic class for multiplying two factors however we have not done the work to generate these random factors yet.

If you try to run all the tests instead of just MultiplicationServiceTest, you’ll get an error (No qualifying bean of type 'microservices. book.multiplication.service.RandomGeneratorService' available). 
The reason is that, by default when you create the app from spring Initializr, the package includes an empty SocialMultiplicationApplicationTests that tries to load the full application context. 
The same thing happens if you try to run the application. When loading the context, spring will try to find an implementation of RandomGeneratorService to inject, but there is none. 
This doesn’t mean you’re doing cowboy development, you’re just using an advantage of tDD—you test as you develop, even if you don’t have the full application up and running yet.
