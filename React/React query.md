# Explanation

## What? and Why?

- a library for managing remote state
- improves UX
    - make site faster
        - caches stored data: aka. [Memoization](Memoization.md)
            - data became avaliable offline
        - pre-fetch for faster data load (e.g. pagination)
    - provides loading, and erros states
    - easy mutation for remote state
    - automatic re-fetching to keep data in sync

## Methods

- to fetch data we use useQuery
    - we pass a query key
- to write data we use useMutation
    - onSuccess we invalidate key to enable refetch
- [queries & mutation abstraction](queries%20&%20mutation%20abstraction.md)

# Sources
