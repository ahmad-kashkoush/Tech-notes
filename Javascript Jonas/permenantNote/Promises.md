## What is a Promise?

1. It is container for future value
2. all the code will continue working regardless of of promise gets its value or not

## Promise lifecycle

![Promise LifeCycle](Promise%20LifeCycle.png)

1. using ==fetch api== builds the promise
2. Then I can [Programming/Javascript Jonas/consume promises](Programming/Javascript%20Jonas/consume%20promises) as much as I want

## Promise Combinators

- Some Promise Combinators, or Methods
    - _Promise.all()_:
        - make all await calls run at the same time
        - return an array of calls that are resolved
        - If there is a rejected then it will return an error
    - _promise.race()_:
        - returns the first settled call
        - either rejected, or fullfilled
        - I can use it also to set timeout if requests are taking too long
    - _promise.allSettled()_:return all calls either rejected or resolved
    - _promise.any()_:returns an array of only resolved
# Sources
