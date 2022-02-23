---
layout: post
title: Spring There and Back Again — An Unexpected Development Journey
tags: dev, solarnet
category: news
---
## Some Perspective

SolarNetwork has been around for a wee while at this point. When we started around **2006** when
**Java 6** had just been released, as had **Spring Framework 2**. As with many software projects,
SolarNetwork started out pretty small in scope. Both the server-side SolarNet application and the
distributed SolarNode application were fairly simple Java + Spring applications. Another Java
technology was being enthusiastically embraced by many (including the Spring developers): **OSGi**.
OSGi was a great fit for SolarNode, so we refactored that into a fully OSGi-based application.

After that was done, OSGi was starting to gain traction for server-side development and application
servers popped up, including the **Spring Source dm Server**. We decided there would be some nice
benefits to unifying the SolarNode and SolarNet development stacks in the OSGi world, so we jumped
in and refactored all of SolarNet (which had grown considerably into a suite of applications) into
OSGi modules, deployed on dm Server. Eventually Spring donated the dm Server code to the Eclipse
Foundation, and it became the **Virgo Server**, which we switched over to using for SolarNet.

## Fast Forward

Time continued marching forward, and unfortunately a lot of the enthusiasm for server-side OSGi
development petered out. Yes there is Apache Karaf, which is a great product, but Virgo development
has all but ceased. Spring stopped supporting OSGi in Spring Framework 3.2, around 2012. The Spring
community has also evolved quite a bit, with enthusiasm coalescing around the Spring Boot project
around 2014.

It was time to reassess the SolarNet reliance on Virgo, and OSGi more generally. Note that OSGi is
still a great fit for SolarNode, which is a highly flexible plug-in based environment.

## We're Back

After thinking about how SolarNet should evolve based on the reality on the ground, so to speak, we
settled on porting SolarNet _back to Spring applications_ (Spring Boot, more specifically). Work
started in Q4 2021, and because dropping OSGi-isms from SolarNet was a fairly big change, we took
the opportunity to update the applications to use more modern toolkits. For example:

| SolarNet 1.0 | SolarNet 2.0 | Description |
|:-------------|:-------------|:------------|
| Java 6       | Java 11 | The Java runtime used |
| Joda Time    | `java.time` (Java 8 Time) | Date/time parsing |
| Spring 4.3   | Spring 5.3 | Uber Java support framework |
| Virgo 3.7    | Spring Boot 2.6 | Application configuration and deployment |
| JSP 2.1      | Thymeleaf 3.0 | HTML rendering |
| MyBatis 3.5  | Spring JDBC<sup>†</sup> | SQL database integration |
| Any + Ivy    | Gradle | Build framework |

It was a big undertaking, but now SolarNet is much more aligned with modern Java development
practices and will be much easier to maintain, and evolve, going forward.

🎉 

<sup>†</sup> MyBatis is still used, but is being phased out over time.
