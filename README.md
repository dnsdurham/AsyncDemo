# Async Demo

## Tutorial
https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/

## Common async scenarios
https://docs.microsoft.com/en-us/dotnet/csharp/async

## Objective
You should write code that reads like a series of synchronous statements.

## Make Breakfast
Pouring coffee
**coffee is ready**
Warming the egg pan...
cracking 2 eggs
cooking the eggs ...
Put eggs on plate
**eggs are ready**
putting 3 slices of bacon in the pan
cooking first side of bacon...
flipping a slice of bacon
flipping a slice of bacon
flipping a slice of bacon
cooking the second side of bacon...
Put bacon on plate
**bacon is ready**
Putting a slice of bread in the toaster
Putting a slice of bread in the toaster
Start toasting...
Remove toast from toaster
Putting butter on the toast
Putting jam on the toast
**toast is ready**
Pouring orange juice
**oj is ready**
Breakfast is ready!


## Make Breakfast Async
`Pouring coffee
**coffee is ready**
Warming the egg pan...
cracking 2 eggs
cooking the eggs ...
Put eggs on plate
**eggs are ready**
putting 3 slices of bacon in the pan
cooking first side of bacon...
flipping a slice of bacon
flipping a slice of bacon
flipping a slice of bacon
cooking the second side of bacon...
Put bacon on plate
**bacon is ready**
Putting a slice of bread in the toaster
Putting a slice of bread in the toaster
Start toasting...
Remove toast from toaster
Putting butter on the toast
Putting jam on the toast
**toast is ready**
Pouring orange juice
**oj is ready**
Breakfast is ready!`

## Make Breakfast Concurrent
`Pouring coffee
**coffee is ready**
Warming the egg pan...
putting 3 slices of bacon in the pan
cooking first side of bacon...
Putting a slice of bread in the toaster
Putting a slice of bread in the toaster
Start toasting...
cracking 2 eggs
cooking the eggs ...
flipping a slice of bacon
flipping a slice of bacon
flipping a slice of bacon
cooking the second side of bacon...
Remove toast from toaster
Putting butter on the toast
Putting jam on the toast
**toast is ready**
Pouring orange juice
**oj is ready**
Put bacon on plate
Put eggs on plate
**eggs are ready**
**bacon is ready**
Breakfast is ready!`

## Make Breakfast Composition
`Pouring coffee
**coffee is ready**
Warming the egg pan...
putting 3 slices of bacon in the pan
cooking first side of bacon...
Putting a slice of bread in the toaster
Putting a slice of bread in the toaster
Start toasting...
cracking 2 eggs
cooking the eggs ...
flipping a slice of bacon
flipping a slice of bacon
flipping a slice of bacon
cooking the second side of bacon...
Remove toast from toaster
Putting butter on the toast
Putting jam on the toast
Put eggs on plate
**eggs are ready**
Put bacon on plate
**bacon is ready**
**toast is ready**
Pouring orange juice
**oj is ready**
Breakfast is ready!`

## Make Breakfast Exception
`Pouring coffee
coffee is ready
Warming the egg pan...
putting 3 slices of bacon in the pan
cooking first side of bacon...
Putting a slice of bread in the toaster
Putting a slice of bread in the toaster
Start toasting...
**Fire! Toast is ruined!**
flipping a slice of bacon
flipping a slice of bacon
flipping a slice of bacon
cooking the second side of bacon...
cracking 2 eggs
cooking the eggs ...
Put bacon on plate
Put eggs on plate
eggs are ready
bacon is ready
Unhandled exception. System.InvalidOperationException: The toaster is on fire
   at MakeBreakfastAsyncException.Program.ToastBreadAsync(Int32 slices) in /Users/dougdurham/Documents/GitHub/dnsdurham/AsyncDemo/AsyncDemo/MakeBreakfastAsyncException/Program.cs:line 63`

## Make Breakfast Efficient Await
`Pouring coffee
**coffee is ready**
Warming the egg pan...
putting 3 slices of bacon in the pan
cooking first side of bacon...
Putting a slice of bread in the toaster
Putting a slice of bread in the toaster
Start toasting...
cracking 2 eggs
cooking the eggs ...
flipping a slice of bacon
flipping a slice of bacon
flipping a slice of bacon
cooking the second side of bacon...
Remove toast from toaster
Putting butter on the toast
Putting jam on the toast
**toast is ready**
Put eggs on plate
Put bacon on plate
**bacon is ready**
**eggs are ready**
Pouring orange juice
**oj is ready**
Breakfast is ready!`

