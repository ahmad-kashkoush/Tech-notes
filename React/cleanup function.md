# Explanation

- function that is executed in two ocasions:
    1.  before [useEffect](useEffect.md) get executed again
    2.  after componenet has unmounted
- Clean up function
    - is neccessary to prevent side effect from keep hapening when the componenet is re-rendered or unmounted
    - is neccessary also to prevent calling multiple requests over eacher other which is [Race Condition](../../Database/CS50%20SQL/Race%20Condition.md) , By Cancelling previous request so that the new one will be consumed only
        - Without cleanup request overlab ![before clean up function](before%20clean%20up%20function.png)
        - With Cleanup function![after cleanup function](after%20cleanup%20function.png)
            - only last request is accepted
            - Cancelled all requests before last request which is the needed one
    - Is necessary also to prevent _accumulative event Listener_ Issue
        - By just removing the events on unmount and re-render
- Why If you add a state values in the cleanup function they will be remembered? isn't the componenet and its states are mounted or destoryed?
    - Answer is because of [closure](closure.md) which is a javascript concept
-

## Potential Cleanup

    ![potential cleanup](potential%20cleanup.png)