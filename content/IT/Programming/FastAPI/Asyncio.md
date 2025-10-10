---
tags:
  - it/ProgrammingLanguages
---
[Russian Tutorial 1H](https://youtu.be/h-EFkclgCc8?si=3Rql0NN_6uZkyhpl)
[Tech With Tim](https://youtu.be/Qb9s3UiMSTA?si=cYPJATD3JQCwkPyB)

[[c4 model]]


```mermaid
    C4Context
      title AsyncIO
  
    ContainerDb(c4, "Database", "Relational Database Schema", "Stores user registration information, hashed authentication credentials, access logs, etc.")
    Container(c1, "Single-Page Application", "JavaScript and Angular", "Provides all of the Internet banking functionality to customers via their web browser.")
    Container_Boundary(b, "API Application") {
      Component(c3, "Security Component", "Spring Bean", "Provides functionality Related to signing in, changing passwords, etc.")
      Component(c2, "Sign In Controller", "Spring MVC Rest Controller", "Allows users to sign in to the Internet Banking System.")
    }
    Rel(c1, c2, "Submits credentials to", "JSON/HTTPS")
    Rel(c2, c3, "Calls isAuthenticated() on")
    Rel(c3, c4, "select * from users where username = ?", "JDBC")

    UpdateRelStyle(c1, c2, $textColor="red", $offsetY="-40")
    UpdateRelStyle(c2, c3, $textColor="red", $offsetX="-40", $offsetY="60")
    UpdateRelStyle(c3, c4, $textColor="red", $offsetY="-40", $offsetX="10")


```

> [!info]
> Instead of giving A+B+C we can take max(A, B, C)




| Sync            | Async          |
| --------------- | -------------- |
| Start ➡️ Finish | Start➡️Start➡️ |
| Start ➡️ Finish | Finish➡️Finish |

## Components
- Function that may pause - Async similar to [Generators](https://www.geeksforgeeks.org/python/generators-in-python/)
- In function point where to pause - Await
- Pause/Resume manager - Event loop (`asyncio.run()`)


Coroutine ➡️ <mark style="background: #BBFABBA6;">Can</mark> pause and resume
Subroutine  ➡️  Control given to subroutine. After it finishes control returns back to main thread (<mark style="background: #FF5582A6;">Can't</mark> pause and resume)
Routine 


Concurrency vs Parallelism
![[Concurrency_vs_Parallelism_better.png]]
![[Concurrency_vs_Parallelism.png]]



> Use 'await' with 'awaitable' commands
> Any function that has 'await' keyword must be declared 'async'




## Event loop

