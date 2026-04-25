# DAD 220 — Introduction to Structured Database Environments

Completed: June 2026

## Topics covered
- Relational database design — structuring data using
  entities, relationships, and normalization principles
- SQL fundamentals — creating, updating, inserting, and
  deleting data using core SQL commands
- Query construction — writing SELECT, WHERE, and JOIN
  queries to retrieve and analyze data
- Data aggregation — summarizing and grouping data to
  satisfy specific business analysis requirements
- Schema creation — designing and building database
  structures including tables and relationships
- Database administration — creating and managing
  databases and tables in MySQL
- Data analysis — interpreting query results to address
  real-world data requirements

## Tools used
- **MySQL** — primary database management system for
  all labs and projects
- **zyBooks** — interactive platform for hands-on
  learning and weekly practice exercises

## Projects completed

### Project 1 — Database creation from scratch
Designed and built a relational database from the
ground up. Applied normalization principles to
structure entities and relationships, created schema,
and populated tables with data.

### Project 2 — Data analysis project
Performed analysis on an existing dataset using SQL
queries. Constructed SELECT, WHERE, JOIN, and
aggregation queries to answer specific business
requirements and interpreted results.

### Weekly SQL labs
Applied SQL to real-world datasets through weekly
hands-on labs covering each major concept — table
creation, data manipulation, joins, and aggregation.

## What I understand now that I didn't before
- Structured data is everywhere in security. Logs,
  alerts, network flows, and threat intelligence
  feeds are all structured data. Understanding how
  to query structured data efficiently is a practical
  skill that appears constantly in security operations.
- JOIN operations reveal relationships between data
  sets that are not visible when looking at tables
  individually. This is directly applicable to
  correlating events across multiple log sources —
  connecting a network connection log to a process
  creation log to a file write log to reconstruct
  what happened during an incident.
- Normalization is about reducing redundancy and
  maintaining integrity. Those same principles —
  single source of truth, consistent structure —
  apply to how security teams maintain threat
  intelligence databases and IOC repositories.
- Query construction is a form of structured thinking.
  Defining exactly what you are looking for, where
  it lives, and what conditions it must meet is the
  same logical precision required when writing YARA
  rules or Splunk SPL queries.

## Connection to malware analysis
- **SQL query skills transfer directly to Splunk SPL.**
  Splunk's Search Processing Language follows the
  same logical structure as SQL — filtering with
  WHERE-equivalent conditions, aggregating with
  stats commands, and joining data sources. DAD 220
  built the query thinking that makes SPL intuitive.
- **Database skills connect to threat intelligence
  platforms.** Tools like MISP store indicators of
  compromise in structured relational databases.
  Querying IOC databases to find related indicators,
  filter by threat actor, or aggregate by malware
  family uses exactly the skills built in DAD 220.
- **JOIN logic connects to log correlation.**
  Correlating events across multiple log sources
  during malware incident analysis is conceptually
  identical to joining tables in SQL — matching
  records from different sources on a common field
  such as timestamp, IP address, or process ID.
- **Data analysis methodology connects to malware
  behavioral analysis.** Querying data to answer
  specific questions — what happened, when, on which
  system, involving which network connections — is
  the same analytical approach used when reconstructing
  malware activity from forensic artifacts.
- **Schema design connects to building analysis tools.**
  When writing Python tools that store analysis
  results — hashes, behavioral observations, network
  indicators — understanding how to structure that
  data in a database rather than flat files makes
  the tools more useful and queryable.

## What I want to go deeper on
- Splunk SPL specifically — applying SQL-style query
  thinking to security log analysis and building
  correlation searches that detect malware behavior
  patterns across multiple log sources
- Database-backed threat intelligence — how platforms
  like MISP structure and query IOC data and how
  analysts interact with those databases during
  malware investigations
- SQLite in Python — using Python's built-in SQLite
  library to store and query malware analysis results
  programmatically, connecting DAD 220 database skills
  to the Python tooling work in Phase 2
