# Explanation

- Fiber Tree
    - A Tree Initialized on initial Render
    - An internal Tree that has [Reconciler](Reconciliation.md) for each componenet
    - a mutable Data structure
    - States and Probs are stored in the fiber tree
- Stores data [Virtual Dom](Virtual%20Dom.md) as Linked list data structure
    - where parent->next=child, and child->next=sibling in the same componenet and so on
    - Storing data as Linked list Makes Updating component operation take o(1)
- Illustration: ![Fiber Tree](Fiber%20Tree.png)
