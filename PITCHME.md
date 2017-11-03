## Microservices

---
Overview:<br>
- What are microservices?<br>
- Why are they so good?<br>
- Best Practices<br>

---
What are Microservices?
+++
![Image-Absolute](https://help.mypurecloud.com/wp-content/uploads/2016/02/mono-vs-micro.png)
+++
What are Microservices?

"Small, autonomous services  that work together"<br>

- They are small.<br>
- They do one thing.<br>
- They are autonomous.<br>

---
Why use them?
- You can mix up technology:<br>
  - Use the best tool for the job instead of something that "works" for everything.<br>
  - Speed up adoption of new technology. Test out a new technology on a low-risk service first before a wider roll-out.<br>
+++
- Resilience:<br>
  - If a monolith fails, everything can go down.<br>
  - When something goes wrong in a microservice, it is easier to contain it to that service.<br>
  - By building services to handle the "total failure" of other services, you can plan how your system degrades.<br>
+++
- Scaling:<br>
  - Allocate resources to the services that need it most.<br>
+++
- Ease of Deployment:<br>
  - In a monolith, you must deploy the whole app in order to put one change into production. As this is high risk, changes will likely build up until we make one big release.<br>
  - Microservices can be deployed with much lower risk. Deploys are typically more frequent, making it easier to isolate bugs, and get updates to users more quickly.<br>
+++
- Team Organization:<br>
  - Divvy up a large codebase to smaller teams. Keeps people from stepping on each other's toes. Provides benefits of colocation to a larger, spread-out team.<br>
+++
- Reusable:<br>
  - Smaller, single-responsibility applications are easier to re-use. Monoliths don't expose their finer-grained innards.<br>
+++
- Replaceable:<br>
  - Smaller compartmentalized applications are easier and less risky to replace.<br>
  - Monoliths can become little-understood legacy systems that everyone knows should be replaced but nobody wants to.<br>
      
---
Drawbacks:
  - More complicated. 
  - Teams need to be better at deployment and monitoring.
  - More decisions to make.

---
##Best Practices:
- Loose Coupling
  - Services should know as little as possible about the services they collaborate with.
- High Cohesion
  - Place related behavior in the same spot. A change in functionality requires fewer, more localized code changes.
- Bounded Context
  "specific responsibility enforced by explicit boundaries"
+++
- Shared and Hidden Models
  - Some models might be necessary for services to communicate, some are isolated to a single service.
  - Keeping non-essential details hidden naturally promotes decoupling and cohesion.
-System Architecture
  "Be worried about what happens between the boxes, and be liberal in what happens inside."
- Avoid Premature Decomposition
   - Don't break servies down before the boundaries are clear. You may have to make expensive changes down the road if the boundaries aren't appropriate.
