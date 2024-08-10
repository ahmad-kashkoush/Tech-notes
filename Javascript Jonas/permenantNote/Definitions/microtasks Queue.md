- microtasks code is going to be executed _before_ callback queue code.
- so fetching promises have higher prioirty than other events.
    ![Asynchronous Behind the scenes](Asynchronous%20Behind%20the%20scenes.png)
