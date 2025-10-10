#it/cybersecurity/CISSP

## When security should be considered
?
> Security must be included in **each step** of the SDLC
> Security must be built into the system **as early as possible**

## Programming language Types ✅
?
- Machine language - 0101
- Assembly - mnemonics (mov, add)
- High-level - processor independent 
- Very high-level - focus on algorithm (python, C++, Java ...)
- Natural - learn and change on its own (AI) 
## 7 Software Development Methodology
![[Software_Development_Methodology.png]]
- Initiation & risk analysis
- Functional design analysis and planning
- system design specifications
- Software development - write code
- Installation / test / implementation
- Operational / maintenance / (Incidents & Updates)
- Disposal - End of life

- Build and fix
- Waterfall (6 steps)![[waterfall_method_of_development.png]] ![[waterfall_pro_con.png]]
	- Project initiation & risk analysis
	- Requirements
	- Design
	- Develop
	- Testing
	- Deployment
	- Maintenance



- V-Shaped
- Prototyping
- Incremental
- Spiral
- Rapid Application Development (RAD)
- Agile ![[agile_method_of_development.png]] ![[agile_pro_con.png]]
## Threat Modeling
- Data Flow Diagrams
- [[Misuse Cases]]
- [[S.T.R.I.D.E.]]
- [[Attack Trees]]
- Reduce [[Attack Surface]]

## Application Threat
- Code injection - input validation
	- SQL
	- DLL
	- LDAP
	- XML
	- XSS
		- Stored
		- Reflected / non-presistent
		- Dom based
	- xsrf
	- Timing attacks
		- Physical Access - Before sec requirements arrived
		- Race Condition - Technical timing exploit
		- TOC/TOU - Time of check / Time of use
	- Buffer/integer overflow
	- Memory leaks
- 
## DB Threats ❓❓
?
- **Aggregation**:  
    Combining non-sensitive data to ==derive sensitive information==.
    - **Example**: Individually accessible salaries and job titles can reveal an organization's pay structure.
    **Mnemonic**: "Small pieces, big secrets."
- **Inference**:  
    Deducting sensitive data from ==query results or patterns==.
    - **Example**: Knowing who attended a meeting by querying "Who took lunch after the meeting?"
    **Mnemonic**: "What’s implied hides inside."
- **Access Control**:  
    Limiting who can access what data, based on rules.
    - **Threat**: Weak or misconfigured controls let unauthorized users access data.
    **Mnemonic**: "Who's in, who's out."
- **Access Control Mechanisms**:  
    The tools used to enforce access control.
    - **Examples**: Role-based access control (RBAC), mandatory access control (MAC).
    - **Threat**: Flaws in these mechanisms can allow bypassing restrictions.
    **Mnemonic**: "Locks that mustn’t fail."

## A.C.I.D. ❓
?
- Atomicity - All or nothing
- Consistency - from one valid state to another (Valid state transitions)
- Isolation - Isolated package (Transactions don’t interfere)
- Durability - Once committed, always there

## APIs
- SOAP - xml
- RESTful - json
- Supply chain
## Cohesion and Coupling 
![[cohesion_vs_coupling.png]]
## Covert Channels❓❓
methods used to transfer information in ways that violate a system's security policy.


- Executable content mobile code
- Virus
- Worm
- Logic Bomb / Code Bomb
- [[Buffer overflow]]
- Backdoor
- Covert channel
- [[Botnet]] - A network of computers infected by malware 
	- Botmaster
	- Zombies
	- Spamming
	- Spyware
	- Dial-up bots
	- Web crawler
- Trojan
## Virus types ❓❓
- Boot sector
- System infector
- UEFI
- Companion
- Stealth
- Multipart
- Self-garbling
- Polymorphic
- Resident
- Master Boot Record / Sector (MBR)

## Anti-virus types ✅
- Signature based - detects known malware only
- Heuristic based - Static analysis



#todo Know nothing about it.
## TCB - Trusted Computer Base ❓❓
The set of all 
- hardware, 
- firmware,
- software components 
that are critical to its security. 

Any compromises here are critical to system security.

Input/output operations
execution domain switching
Memory protection
process activation


## Knowledge management ❓
- Expert systems
	- Knowledge base
	- Inference engine
	- Use human reasoning
	- Rule based knowledge base
	- If-then statement
	- Inference System
- Expert systems (Two modes)
	- Forward chaining
	- Backward chaining
- Neural Networks
	- Observing events
	- Predicts outcomes
	- Multiple iterations


## Database systems ❓
- Database - Define storing and manipulating data
- DBMS - Software program control access to data stored in a database.
- DBMS Types
	- Hierarchical 
	- Network 
	- Mesh 
	- Object-orientated 
	- Relational
- **DDL** - Data definition language defines structure and schema DML
- **DDE** - Dynamic data exchange
- **DCL** - Data control language. Subset of SQL.
- **Tuple** - row
- **Degree of Db** - number of attributes (columns) in table
- **Semantic integrity** - ensure semantic rules are enforced between data types
- **Referential integrity** - all foreign keys reference existing primary keys
- **Candidate key** - an attribute that is a unique identifier within a given table, one of the candidates key becomes primary key and others are alternate keys
- **Primary key** - unique data identification
- **Foreign key** - reference to another table which include primary key. Foreign and primary keys link is known as referential integrity
- DBMS Terms 
	- **Incorrect Summaries** - calculating totals on unstable, changing data
	- **Dirty Reads** - reading a draft that might be erased 
	- Lost Updates - last one overwrites the first
	- **Dynamic Lifetime Objects**: Objects developed using software in an Object Oriented Programming environment. 
	- **ODBC** - Open Database Connectivity. Database feature where applications to communicate with different types of databases without a program code. 
	- **Database contamination** - Mixing data with different classification levels 
	- Database partitioning - splitting a single database into multiple parts with unique contents 
	- [[Polyinstantiation]] - two or more rows in the same relational database table appear to have identical primary key and different data in the table. [Youtube](https://youtu.be/YqFhKlzAABE?si=RVsXuXxtbnM9xd5b)


**Remote journaling (log shipping)** - backing up not an entire database but transactions to another site allowing rollback or restore

