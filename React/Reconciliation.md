# Explanation

- When Componenets are re-rendered, You need to keep elements that doesn't change as they are
- So _Reconcilation Proccess_ Wants to Use as much current Dom as possible
- The dom won't be all updated, the only changed ones
- _Reconciler_
    - Decides which dom element to be updated
    - Called Fiber
- So We Reconcile Current [Virtual Dom](Virtual%20Dom.md) with [Fiber Tree](Fiber%20Tree.md)
- Illustration: ![Fiber Tree](Fiber%20Tree.png)
