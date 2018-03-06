
JPA - Java Persistence API
ORM - Object Relational Mapping 

JPA 2.0 + Hibernate 4.0/3.0
JBoss acquired Hibernate

JPQL - Java Persistence Query Language
HQL

Why JPA?
DataModel does not line up with Object Model
Configuration is better: Trasaction, Testing, DS configuration
JPA removes boilerplate code

==JPA providers== (some are datawarehousing and some are lazy loading)
- JBoss Hibernate
- Apache OpenJPA
- TopLink
- EclipseLink
- DataNucleus
- Versant

==JPA configuration==
- POJO based configuration
- XML based configuration
- Annotation based configuration

# LocalContainerEntityManagerFactoryBean
# Dialect is what db - my sql, oracle, etc.,
# Format sql
# hdm2ddl.auto -- create, create-drop, update, validate, none
## --> create-drop --> create DB during appliaction startup & drop after application stop. ##


==Entity==
POJO

@ Entity
@ Table
@ Id
@ GeneratedValue	IDENTITY / AUTO / SEQUENCE / TABLE
@ Column	(insertable, length, name, nullable, precision, scale, table, unique, updatable) --> descriptive information

@ PersistenceContext a.k.a EntityManager -- injects entity manager into our code
@ Service
@ Repository
@ Trasactional
@ NamedQueries ({
	@NamedQuery = (Name="findGoals", query="select * from..."),
	@NamedQuery = (Name="findAllGoals", query="select * from...")
})

==Design Patterns==

==Trasaction==
@OneToOne
@OneToMany	(most common)
@ManyToOne
@ManyToMany

configs...
Unidirectional
Bidirectional
Cascade

==Fetch Types==
- Lazy - Query the db when property is called
- Eager - Query the db when the object is originally created

Spring Data JPA




