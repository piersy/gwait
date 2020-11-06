# goroutine-waiter
A simple utility to de-duplicate the job of waiting for goroutines to close

```go
	w := gwait.NewWaiter()

	// Run function in a goroutine
	w.Go(func() {
		// do something
	})

	// Run another function in a goroutine
	w.Go(func() {
		// do something else
	})

	// Ensure we wait for the goroutines to complete
	w.Wait()
```
