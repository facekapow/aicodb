# AicoDB
A performant, machine-learning-enhanced database

AicoDB is a database written with maximum performance in mind. In addition to making the plain database system as fast as possible to use on its own, a major part of AicoDB is its psuedo-machine-learning components that allow it to predict how you'll use the database and make it even faster.

## FAQ

### Q: Machine learning? In a database? How does that work?
Well, it's not exactly machine-learning per-se. It's more of a psuedo-machine-learning. There are no big, official, math-backed algorithms being used; instead, it collects various kinds of data and stores it locally, leaving it another thread to analyze it in the background. This analyzer tries to find patterns in the accesses such as when the requests occurred, what other requests were subsequently made, who made the requests, and much more.

These patterns are then applied to automatically make requests in anticipation of their use. If the pattern holds up, then we just pass on the data when the request is finally made and we have successfully improved response time. Otherwise, the request is fulfilled normally and the prefetched data is discarded, incurring no more penalty than a pattern-less access would've incurred.
