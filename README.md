### Creating Threads.

Expected time required: 15 min

We are developing software that is sorting packages in an Amazon warehouse. We have a main thread in
`WarehouseApp` that sends data on new deliveries to `DeliveryManager`. `DeliveryManager` currently
is just a new class, but we are planning on adding deeper functionality to it, and so we need to
update it to implement a `Runnable` interface in preparation for this.

The program currently gets a delivery that gets sent to `DeliveryManager`, which then sorts out the
packages into `incomingPackages` and `additionalProcessing` lists. Each list then has its contents
printed. The sorting and printing should happen in a new thread, which is started in a method in
`WarehouseApp` called `startDeliveryThread`.

The steps that need to be completed are as follows:

1. Run `WarehouseAppTest` and save the output.
2. `DeliveryManager` needs a `Runnable` interface. 
3. Complete the `run()` method in  `DeliveryManager` so it handles the sorting and printing. The
   constructor of `DeliveryManager`  should only initialize the lists.
4. In `WarehouseApp`, complete `startDeliveryThread()`, which starts up the thread. `main` should
   only contain the printout line and a call to `startDeliveryThread()`.
5. Re-run `WarehouseAppTest` and verify that the new output matches the output from step 1.



HINTS:
You may need to move around some method calls to have the output in step 5 match that of step 1.
* [I don't know what code to move?](hints/hint-01.md)
