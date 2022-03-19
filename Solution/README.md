### Creating Threads.

**Branch name:** introthreads-prework

**RDE workfows:**
* `rde wflow run introthreads-prework-creatingthreads-warehouseapp`
* `rde wflow run introthreads-prework-creatingthreads-warehouseapptest`

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

1. `DeliveryManager` needs a `Runnable` interface. 
2. Complete the `run()` method in  `DeliveryManager`  to handle the sorting and printing. The constructor of
    `DeliveryManager`  should only have code initializing the lists.
3. In `WarehouseApp`, complete `startDeliveryThread()` to start up the thread. `main` should only have the printout
    line and a method call to `startDeliveryThread()`.

Some method calls may need to be moved around. The output should be the same after adding threads, so check what it
looks like before starting to code.

HINTS:
* [I don't know what code to move?](hints/hint-01.md)
