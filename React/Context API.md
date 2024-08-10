# Explanation

- a system to pass data to a very nested child without passing it to middle children
- Helps avoid [Prob Drilling Issue](Prob%20Drilling%20Issue.md)
- ![Pasted image 20240424130130](Pasted%20image%2020240424130130.png)

## Factors of Context API

- _Provider_: broadcast global value to entire app
- _Value_: values that is accessed through the app
- _Consumer_:
    - a component that provided context value
    - will be re-rendered when value is updated
