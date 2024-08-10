# Explanation

- simple abstraction to a [Custom hooks](Custom%20hooks.md)

## make properties abstract

try to make your code abstract and generic as much as you can

- mutation before

```js
   mutationFn: insertCabin,
        onSuccess: () => {
		    // ⭐ keep here common actions
            toast.success("cabin successfully updated");
            queryClient.invalidateQueries({
                queryKey: ["cabins"],
            });
// the following 2 actions is scoped
// so it's better to pass them to the mutate, not here
            // reset();
            // onCloseForm();
        },
        onError: (err) => toast.error(err.message),
    });
```

- mutate call

```js
updateCabin(
        { updatedCabin},
        {
          onSuccess: () => {
            reset();
            onCloseForm();
          },
        }
      );
```
