# IT 145 — Foundation in Application Development (Java)

Completed: April 2026

## Topics covered
- Object-oriented programming in Java — defining classes,
  creating objects, using constructors, and implementing
  inheritance
- Polymorphism — same interface producing different
  behavior depending on which object is called at runtime
- Data structures — working with ArrayList to manage
  collections of objects programmatically
- Control structures — conditional statements and loops
  for program logic and flow control
- Software Development Lifecycle (SDLC) — phases from
  requirements through testing in an agile environment
- Eclipse IDE — developing, debugging, and managing
  Java projects in a professional development environment
- Best practices — clean code standards including
  proper indentation, descriptive variable naming,
  and detailed commenting for documentation
- Interactive application development — writing,
  reviewing, and documenting functional Java applications
- UML class diagrams — reading and implementing class
  structure from professional specification documents
- Pseudocode and flowcharts — planning program logic
  before implementation using industry standard tools

## Tools used
- **Eclipse IDE** — primary development environment
  for all Java projects and debugging
- **Codio** — virtual lab environment for project
  development and submission

## Projects completed

### Project 1 — Pet BAG pet boarding system (Global Rain)
Designed and developed software for Pet Boarding and
Grooming (Pet BAG) as part of a simulated development
team at Global Rain software engineering company.

**What I built:**
- Created Pet.java class from scratch based on a UML
  class diagram — implementing all attributes with
  appropriate data types, a full constructor initializing
  all values, and accessors and mutators for every attribute
- Wrote pseudocode planning out either the pet check-in
  or check-out method in logical, organized steps
- Created a flowchart showing decision branching and
  program flow for the selected method
- Wrote a summary report explaining how OOP principles
  including encapsulation and inheritance were applied

**Key concepts demonstrated:**
- Class creation from a UML diagram specification
- Encapsulation — attributes with accessors and mutators
- Constructor implementation with parameter initialization
- Professional pseudocode and flowchart documentation
- Explaining OOP principles in plain language for
  a non-technical audience

### Project 2 — Grazioso Salvare animal tracking system
Developed software for a fictional international
search-and-rescue animal training company called
Grazioso Salvare as part of a simulated professional
development team at Global Rain.

**What I built:**
- Created Monkey.java from scratch — a new class inheriting
  from the RescueAnimal parent class with all attributes,
  a full constructor taking all values as parameters, and
  accessors and mutators for every attribute
- Modified Driver.java to implement a menu-driven application
  with input validation, intake methods for dogs and monkeys,
  an animal reservation system, and a print method displaying
  available in-service animals
- Managed two ArrayLists — one for dogs, one for monkeys —
  adding, searching, and updating objects programmatically
- Applied industry standard best practices throughout —
  in-line comments, descriptive variable naming, and
  consistent documentation

**Key concepts demonstrated:**
- Inheritance — Monkey extending RescueAnimal
- Polymorphism — same interface handling different animal types
- ArrayList data structure management
- Input validation and menu loop logic
- Professional code documentation standards

## What I understand now that I didn't before
- Polymorphism is the most powerful OOP concept for
  understanding how complex software — including malware
  — is structured. Polymorphism means the same interface
  can produce different behavior depending on which
  object is actually being called at runtime. In malware
  this appears as a single function call that behaves
  differently depending on the target environment,
  the payload loaded, or the C2 instructions received.
  Recognizing polymorphic structure in decompiled code
  is what separates surface-level analysis from
  understanding how the malware actually works.
- Inheritance is one of the most powerful concepts
  in programming. A subclass inheriting from a parent
  means you write common functionality once and extend
  it specifically where needed. Recognizing that
  structure in decompiled Java malware immediately
  tells you what the malware author considered core
  functionality versus specialized behavior.
- Object orientation changes how you think about
  program structure. Instead of a sequence of
  instructions you think in terms of objects with
  properties and behaviors interacting with each
  other. That mental model applies directly to
  reverse engineering — malware is organized into
  functional components just like legitimate software.
- Authentication systems have specific vulnerabilities.
  Building one from scratch revealed exactly where
  authentication logic can fail — hardcoded credentials,
  weak comparison logic, bypassable checks. Those
  same vulnerabilities appear constantly in malware
  that targets authentication systems or implements
  its own.
- Clean code and documentation are professional
  obligations not optional extras. Code that cannot
  be read and understood by another analyst is
  effectively useless in a team environment. The
  documentation habits built in IT 145 apply directly
  to writing analysis reports and tool documentation.
- The SDLC is not just academic process. Malware
  authors follow development processes too — versioning,
  testing, staged deployment. Recognizing a mature
  development process in malware tells you something
  significant about the threat actor behind it.
- UML diagrams are a universal language for software
  design. Reading a UML class diagram and translating
  it directly into working code is a professional
  skill that appears in team-based development
  environments and in reverse engineering when
  reconstructing the architecture of complex malware.

## Connection to malware analysis
- **Polymorphism connects to malware evasion and
  modularity.** Polymorphic malware uses the same
  principle — identical interfaces with different
  underlying behavior — to evade signature-based
  detection by changing its code while maintaining
  its functionality. Understanding polymorphism at
  the source code level is the foundation for
  understanding polymorphic and metamorphic malware
  in Phase 3 of the roadmap.
- **Java OOP connects directly to Android malware
  analysis.** Android malware is Java-based and
  tools like jadx decompile APK files back to
  readable Java source code. Understanding classes,
  inheritance, constructors, and ArrayLists makes
  reading that decompiled code significantly faster
  and more accurate.
- **Authentication system development connects to
  credential-targeting malware analysis.** Building
  an authentication system revealed exactly where
  authentication logic is vulnerable — the same
  weaknesses that malware like credential stealers
  and keyloggers specifically target and exploit.
- **Inheritance structure connects to malware
  family analysis.** Malware families share code
  through inheritance-like relationships — a base
  loader with specific payload subclasses, a core
  C2 module with protocol-specific implementations.
  Recognizing inherited structure in decompiled
  code helps identify malware family relationships.
- **Eclipse debugging connects to dynamic analysis
  methodology.** Stepping through Java code in
  Eclipse to understand program behavior is the
  same methodology used in x64dbg when stepping
  through malware instructions — set breakpoints,
  observe state, follow execution flow.
- **SDLC knowledge connects to threat actor
  assessment.** A malware sample showing evidence
  of structured development — versioning, modular
  design, consistent coding standards — indicates
  a sophisticated threat actor. IT 145 built the
  software development literacy to recognize that
  sophistication when it appears.
- **UML and architecture reading connects to
  malware family mapping.** Reconstructing the
  architecture of a complex malware family —
  identifying modules, understanding relationships
  between components — is the same skill as reading
  a UML diagram. IT 145 built the structural
  thinking that makes that reconstruction possible.

## What I want to go deeper on
- Java bytecode and decompilation — how Java source
  code compiles to bytecode and how jadx reverses
  that process to recover readable source from
  Android malware APK files
- Android malware analysis — applying Java OOP
  knowledge to analyzing malicious Android
  applications, a growing and increasingly
  important malware category
- Authentication bypass techniques — how malware
  and attackers exploit the same vulnerabilities
  in authentication systems that building one
  from scratch revealed
- Polymorphic and metamorphic malware — how malware
  authors apply polymorphism at the code level to
  evade signature detection, covered in depth in
  Evasive Malware in Phase 3
- Java-based malware families — enterprise-targeting
  malware that uses Java for cross-platform
  deployment and how OOP structure appears in
  real malware samples
