# Explanation
- A library for managing remote state
1. Better for UX
    1. Faster site
	    1. By caching stored data
            - data became avaliable offline
        2. pre-fetch for faster data load (e.g. pagination)
2. provides loading,  erros states
3. easy mutation for remote state
4. automatic re-fetching to keep data in sync
5. Method
	1. `useQuery`: for data fetching
	    - we pass a query key
	2. `useMutation`: for data mutating
	    - For refetching we invalidate key in `onSuccess`.
6. Abstracted with [[Custom hooks]] (Code: [[#Code Example]])
# Sources
