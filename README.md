# Queue-101
This is a queue code I played around with that allows the user to keep inserting after de-queuing elements.


______________________________________________________________Simply_______________________________________________________________________

In this code, the enQueue function writes (enqueues) the data element passed to it (int) and afterwards, the pointer moves ahead (increment)to point at the next free index that we can write in.

The deQueue function moves the deleting pointer one index ahead (increment) and if it is full (includes data) it writes zero in it (basically deletting what's in it)

___________________________________________________________What's New______________________________________________________________________

Some functionally has been added to this basic idea where now it allows the user to write data till the queue is full , and when the user dequeues data out of the queue (resulting in free spots) the writting (enqueuing) pointer sees that there are some free spots in the begining of the array; and relocates to be placed at the first free spot. The same process happens with the deleting (dequeuing) pointer. if you fill the array with values and then deueue all of them; it will look back at the first spot in the array and ask 'Did the user write any data there?' if the answer is yes; it will relocated (when you ask it to dequeue again) to it's initial value and it will procced to dequeue the value out of the array.

_______________________________________________________________Robust______________________________________________________________________

The protectNq function assures that the program will not allow the user to add (enqueue) any more elements to the array if it's full. 

Full here is the act of checking if the next element is zero or not. If next element = 0   = not full
                                                                     If next element !=0   = full  (data is stored in it)
As a consequence of the checking that we do in both enQueue and deQueue the deQueue pointer never goes ahead of the enQueue pointer. deQueue pointer will always be one or more steps behind the enQueue pointer (technically thats write even if the enqueue pointer resets back to zero and the dequeue pointer is at 3 for an example; the dequeue pointer is still behind the enqueue's because it will evenually have to increment and reset back to -1).


Check it out and feel free to create a branch with improvements !
