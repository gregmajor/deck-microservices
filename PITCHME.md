## Exploring Microservices
![Microservices](assets/images/microservices.png)

---

## The 30-Second Buzz

Microservices leverage an approach to constructing applications composed of small services that:

@ul
- Have a discreet, singular capability
- Run in their own process
- Encapsulate their own data
- Communicate with other services via contract
- Can be deployed independently
@ulend

---

## Why?

Microservices done _well_ will:

@ul
- Make maintenance easier
- Increase long-term agility
- Scale easier
- Make it easier to adopt new technology
- Lower development risk
@ulend

---

## Does This Code Make My Service Look Big?

<blockquote>"You can drop a mouse down a thousand-yard mine shaft; and, on arriving at the bottom, it gets a slight shock and walks away, provided that the ground is fairly soft. A rat is killed, a man is broken, a horse splashes." -(J.B.S. Haldane, scientist)[https://en.wikipedia.org/wiki/J._B._S._Haldane]</blockquote>

@ul
- TIP: Start small and move fast
- TIP: Make them only as big as need be (or perhaps a tiny bit smaller)
- TIP: Look to Domain Driven Design for help
- TIP: They ain't pets, they're cattle
- TIP: Size really doesn't matter
@ulend

---

## Bounded Contexts and Microservices

<blockquote>"Size and accuracy are inverse properties of any model." -Greg Major, shady character</blockquote>

@ul
- TIP: Remember that a BC is a tool to organize irreconcilable models
- TIP: Find the seams in the language, logic, and data
- TIP: Enforce a ubiquitous language
- TIP: Be _very_ suspect of relationships to other BC's
- TIP: Be wary when a BC merges data from other BC's
@ulend

---

## Data Sovereignty

<blockquote>"Keep it secret! Keep it safe!" -Gandalf, wizard</blockquote>

@ul
- TIP: Make each service autonomous
- TIP: Build a polyglot persistence model
- TIP: Use a surrogate persistence id
- TIP: It's okay to share identity across contexts
- TIP: Do *NOT* cross the streams!
@ulend

---

## Dude, Where's My Data?

<blockquote>"I refuse to let us go down in history as the dudes who destroyed the universe." -Jesse Montgomery, dude</blockquote>

@ul
- TIP: Never *EVER* report off transactional persistence
- TIP: Federate, observe, or even coordinate with an API Gateway
- TIP: Consider CQRS and materialized views
- TIP: Don't underestimate good ol' ETL
- TIP: Embrace eventual consistency
@ulend

---

## Inter-Service Operations

<blockquote>"Be civil to all; serviceable to many; familiar with few; friend to one; enemy to none." -Benjamin Franklin, ladies' man</blockquote>

@ul
- TIP: Watch out for distributed monoliths
- TIP: Ensure idempotency
- TIP: Version each API, message, and contract
- TIP: Keep your messages _lean_
- TIP: Do *not* publish a client
@ulend

---

## You're On OUR Turf Now, Sucka!

<blockquote>"Nothing is so embarrassing as watching someone do something that you said couldn’t be done." -Sam Ewing, author</blockquote>

@ul
- TIP: Master context switching without imprinted behavior
- TIP: Avoid "common" libraries (yes, even _that_ one)
- TIP: Take the time to document your API with tools like (Swagger)[https://swagger.io/]
- TIP: Don't build what doesn't make sense
- TIP: Decouple everything (source control, CI/CD, etc.)
@ulend

---

## Oh No, Not Again

<blockquote>"What the strag will think is that any man who can hitch the length and breadth of the galaxy, rough it, slum it, struggle against terrible odds, win through, and still knows where his towel is, is clearly a man to be reckoned with." -Douglas Adams, author</blockquote>

@ul
- TIP: Use correlation ids (ex: `X-Correlation-Id` header)
- TIP: Employ structured logs like (Serilog)[https://serilog.net/]
- TIP: Aggregate logging with tools like the (ELK Stack)[https://www.elastic.co/elk-stack]
- TIP: Implement _real_ health checks like (App Metrics)[https://www.app-metrics.io/]
- TIP: Aim for the highest signal-to-noise ratio
@ulend

---

## You? I?

<blockquote>“A user interface is like a joke. If you have to explain it, it's not that good”. — Martin Leblanc, founder (iconfinder.com)[https://t.co/IMyHh0kj6T]</blockquote>

@ul
- TIP: Look _hard_ at (Web Components)[https://www.webcomponents.org/]
- TIP: Be agnostic
- TIP: Allocate plenty of time for client-side state management
- TIP: Provide service-hosted frames for testing
- TIP: Establish conventions when you can't isolate (CSS, events, local storage, cookies)
@ulend

---

## Other Stuff

<blockquote>"What's the simplest thing that could possibly work?" -Ward Cunningham, programmer</blockquote>

@ul
- TIP: Lean on container orchestrators like (Kubernetes)[https://kubernetes.io/] or (Amazon ECS)[https://aws.amazon.com/ecs/]
- TIP: Don't build what you should buy (crypto, authentication, payment processing)
- TIP: Use distributed settings with tools like (etcd)[https://coreos.com/etcd/], (Consul)[https://www.consul.io/], or K8S secrets
- TIP: Use feature flags
- TIP: Consider just two environments; production and pre-production
@ulend

---

## Go Be Awesome!

greg@gregmajor.com