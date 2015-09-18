---
layout: engpage
title: Grounding
excerpt: Referential semantics and epistemology
image:
  feature:
---

# Grounding

## SPARQL

[SPARQL is the new King of all Data Scientist’s tools](http://www.datasciencecentral.com/profiles/blogs/sparql-is-the-new-king-of-all-data-scientist-s-tools) (Andreas Blumauer, Sept 9th, 2015 at 11:23pm)

Inspired by the development of semantic technologies in recent years, in the field of statistical analysis the traditional methodology of designing, publishing and consuming statistical datasets is evolving into “Linked Statistical Data”, the associatiin of semantics with dimensions, attributes and observation values based on Linked Data design principles.

The representation of datasets is no longer a combination of magic words and numbers. Everything is becoming meaningful when URIs replace their positions as dereferencable resources, which further establishes the relations between resources implicitly and automatically. Different datasets are no longer isolated and all datasets share a globally, uniquely and uniformly defined structure.

With the [“RDF Data Cube Vocabulary”](http://www.w3.org/TR/vocab-data-cube/) there is already a W3C Recommendation available for linked statistical data . At this point, it is time to start building data-oriented applications and services with the traditional statistical computing languages such as R, while benefiting from the omnipotent semantic power of the SPARQL query language.

Most of the statistical analysis functions are set operations performed on subsets of a dataset (i.e., a slice, a facet, etc.). Calculation is dull machine work but how to group and create a subset is actually the innovation point to produce analytics. Thanks to SPARQL, now this subset can be created from a semantic perspective instead of mathematics and statistics.

Compared to the traditional filtering way using SQL queries, SPARQL queries eliminate the boundaries of data among datasets and among databases.

An example query can be “list the bestsellers of a supermarket for category science fiction movie in year 2014”. Someone may point out that it is also feasible with SQL if the database schema consists of all relevant fields. Well, it is absolutely correct. But what if there are more conditions such as “during weekends, directed by an American director, casted by European actors”? Is it necessary for a supermarket to maintain such data sets? Assume that there is a supermarket of which the boss is a movie fans and he would like to maintain such data and SQL is working perfectly so far. Can we reuse this query, and accordingly the Web application for another supermarket? Here we have good reasons why we use SPARQL. Any accessible resource can be used to construct the query results.

SPARQL is the new King of all Data Scientist’s tools because …

1. SPARQL is close to how human beings actually think about the world.
2. With SPARQL you can query knowledge graphs.
3. SPARQL is based on knowledge models that can combine mindsets of subject-matter experts, data engineers and information architects.
4. SPARQL is to the Semantic Web and the Web in general what SQL is to relational databases.
5. SPARQL is a W3C recommendation and is supported by many different database vendors, so it doesn’t cause lock-in effects as we’ve become used to with various types of SQL engines (which are not standardized at all).
6. With SPARQL you benefit from the potential to make a collection of data sources look and query like one big database.
7. SPARQL provides pattern based search functionality. With such search capabilities you can find out unknown linkages or non-obvious patterns that give you new insights into your data.
8. Not only is SPARQL a standardized query language, also the access via web interfaces is standardized (this is called a SPARQL endpoint). This makes the integration of different data sources a lot easier.
9. SPARQL is also a standardized update and graph traversal language.
10. SPARQL is a standardized protocol producing standardized results, thus making it a complete API alleviating developers from the necessity to reinvent an API with every single application.
11. With SPARQL you can query over structured and unstructured information as a whole.
12. SPARQL allows you to explore data. In contrast to traditional ways to query databases where knowledge about the database schema/content is necessary SPARQL allows you to ask “tell me what is there”.
13. SPARQL property paths offer completely new ways to explore a data set, e.g. by detecting ‘hidden links’ between business objects.
14. With SPARQL you can define inference rules to gain new information from existing facts.


---

