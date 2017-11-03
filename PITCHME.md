## Microservices

---
##Overview:<br>
-What are microservices?<br>
-Why are they so good?<br>
-Best Practices<br>

---
##What are Microservices?

"Small, autonomous services  that work together"

+++
![Image-Absolute](https://help.mypurecloud.com/wp-content/uploads/2016/02/mono-vs-micro.png)
+++
##What are Microservices?

-They are small.
-They do one thing.
-They are autonomous.
  - You should be able to make a change and deploy a service independently.
  - Expose the bare minimum to consumers. Too much sharing increases the amount of coordination required when making chagnes.
  - All communication is via network calls / the provider's API

+++
##Why use them?
    - You can mix up technology
      - Use the best tool for the job instead of something that "works" for everything
      - Speed up adoption of new technology. Test out a new technology on a low-risk service first before a wider roll-out.
    - Resilience:
      - If a monolith fails, everything can go down.
      - When something goes wrong in a microservice, it is easier to contain it to that service.
      - By building services to handle the "total failure" of other services, you can plan how your system degrades.
    - Scaling:
      - Allocate resources to the services that need it most
    - Ease of Deployment
      - In a monolith, you must deploy the whole app in order to put one change into production. As this is high risk, changes will likely build up until we make one big release.
      - Microservices can be deployed with much lower risk. Deploys are typically more frequent, making it easier to isolate bugs, and get updates to users more quickly.
    - Team Organization
      - Divvy up a large codebase to smaller teams. Keeps people from stepping on each other's toes. Provides benefits of colocation to a larger, spread-out team.
    - Reusable
      -Smaller, single-responsibility applications are easier to re-use. Monoliths don't expose their finer-grained innards.
    - Replaceable
      - Smaller compartmentalized applications are easier and less risky to replace
      - Monoliths can become little-understood legacy systems that everyone knows should be replaced but nobody wants to.
      
---
##Drawbacks
  - More complicated. 
  - Teams need to be better at deployment and monitoring
  - More decisions to make.
    "Be worried about what happens between the boxes, and be liberal in what happens inside."

---
##Best Practices:

  - Loose Coupling
    -Services should know as little as possible about the services they collaborate with.
  - High Cohesion
    -Place related behavior in the same spot. A change in functionality requires fewer, more localized code changes.
  - Bounded Context
    "specific responsibility enforced by explicit boundaries"
  - Shared and Hidden Models
     - Some models might be necessary for services to communicate, some are isolated to a single service.
     - Keeping non-essential details hidden naturally promotes decoupling and cohesion
  - Avoid Premature Decomposition
    -Don't break servies down before the boundaries are clear. You may have to make expensive changes down the road if the boundaries aren't appropriate.
