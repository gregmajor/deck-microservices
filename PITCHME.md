# Exploring Microservices
![Microservices](assets/images/microservices.png)
### Tagline Goes Here

---

## The 30-Second Buzz

Microservices is an approach to constructing applications composed of small services that:

@ul
- Have a discreet, singular capability
- Run in their own process
- Encapsulate their own data
- Communicate with other services via contract
- Can be deployed independently
@ulend

---

## Why?

@ul
- Better maintainability
- Increased long-term agility
- Better scalability
- Reduced cost of success
- Lower risk development
@ulend

---

## Singular Capability

@ul
- Size _doesn't_ matter (but make them as small as possible)
- Avoid direct dependencies
- Develop a clear, unambiguous internal model...
@ulend

---

## No, Really. How Big?!?

A good bounded context:

@ul
- Has obvious seams in the language, logic, and data
- Has only a few relationships to other BC's
- Rarely merges data from other BC's to do its primary job
- Is only as big as it needs to be, but should be a tiny bit smaller
@ulend

---

## Bounded Contexts and Microservices

<blockquote>"Size and accuracy are inverse properties of any model."</blockquote>

@ul
- Distill into a ubiquitous language
- Develop a singular model
- Make each service autonomous
- Pssst! It's okay to share identity across contexts
@ulend

---

## Data Sovereignty

@ul
- Each service owns its data and logic
- Match the scope to the service's capability
- Do *NOT* cross the streams!
- Embrace eventual consistency
- Build a polyglot persistence model
@ulend

---

## Go Be Awesome!

greg@gregmajor.com