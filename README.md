# Algorithms
algorithms  JS
// SList: Prepend Val
// Create prependVal(new_val,before_val)
// Given a new_val and a before_val, find the node that has the before_val and insert a new node right in front of it that has the new_val.
// If you can’t find the before_val, put the new node at the end.

prepadVal(3,6)

prepedVal(new_val,before_val)
    var runner = this.head;
    while(runner.val!=before_val){
        newNode.next=null
    
    else
        (runner.val == before_val){
            newNode = before_val
        }
    }

// SList: Append Val
// Create appendVal(new_val,after_val)
// Given a new_val and an after_val, find the node that has the after_val and insert a new node right after it that has the new_val.
// If you can’t find the after_val, put the new node at the end.

prepadVal(3,6)

prepedVal(new_val,after_val)
    var runner = this.head;
    while(runner.val!=after_val){
        newNode.next=null
    
    else
        (runner.val == after_val){
            newNode = after_val
        }
    }

    // Remove Negatives
    // - Find and remove any negative value nodes in the list  
    var runner=this.head;
    while(this.head.val !=null){
        if(this.head.val<0){
            this.head=runner.next;
        }
        else if (runner.next.val<0){
            runner.next = runner.next.next;
        }
        return=runner.next;
    }
    console.log("removed negatives.")

    //////////////////////
    ////Second to last
//     Second to Last Value
// - Find and return the second-to-last value in the list
// - What will you do if the list isn't long enough? What if it only has 1 item? What if it has 2?
    /////////////////

    secondToLast() {
        var runner = this.head;
        if (this.length() >= 2) {
            while (runner != null) {
                if (runner.next.next == null) {
                    console.log("Second to last found: " + runner.val);
                    return runner;
                }
                runner = runner.next;
            }
        } else {
            console.log("List too short, no second-to-last value.");
            return false;
        }
    }

    // BONUS CHALLENGE: Partition
    // - Given a value, find that value in the list
    // - Once found, take every value in the list that's LOWER than that value and move those nodes EARLIER (so, on the LEFT side of the found node)
    // - Take all the values that are greater and move those nodes later (aka to the RIGHT of the found node)
    // - Try making it work for a list with 3 nodes only to start (look for the middle value)
    partition2(someval) {
        var runner = this.head;
        var templow = new SLL();
        var tempequ = new SLL();
        var temphigh = new SLL();
        while (runner != null) {
            if (runner.val < someval) {
                templow.addToBack(runner.val);
            } else if (runner.val > someval) {
                temphigh.addToBack(runner.val);
            }else {
                tempequ.addToBack(runner.val);
            }
            runner = runner.next;
        }
        templow.appendList(tempequ);
        templow.appendList(temphigh);
        this.head = templow.head;
    }


    // Create SLQueue method enqueue(val) to add the given value to end of our queue. Remember, SLQueue uses a singly linked list (not an array).
    class Node{
        constructor(val) {
            this.val = val;
            this.next = nul;
        }
    }

    class SLLQueue {
        constractor() {
            this.head = null;
        }
    }

        // adding
        push(val){
            var newNode= new Node(val);
            var number = this.head;
            while(runner.next !=null){
                runner.next
            }
            runner.next = newNode
        }

        //removing
        pop() {
            var runner = this.head
            while (runner.next.next !=null){
                runner.next = runner.next
            }
            runner.next = null
        }

        printToDisplay() {
            var runner = this.head;
            while (runner.next !=null) {
                console.log(runner.value)
                runner = runner.next
            }
            console.log(runner.value)
        }
    }    

    // Stacks and Queues are companion data structures. Both are sequential, meaning they manage data according to the order in which they were added. A Queue data structure operates by a principle of “First-In becomes First-Out” (FIFO); a Stack is quite the opposite (Last-In, First-Out or LIFO).
    // Consider a pile of papers. With this stack of papers, we can only get a good look at the top of the pile. When we add another paper, that page becomes the only one visible. We can only add and remove papers from the top. We cannot add a page mid-stack (just as one should not cut into the middle of a queue at the ice cream store).

    class arrStack{
        constructor(){
            this.stack=[];
            this.size=0;
        }
        push(val){
            this.stack[this.size]=val;
            this.size++;
        }
        pop_back(){
            this.stock.length-=1;
            this.size--;
        }
        top() {
            return this.stack[this.size-1];
        }
    
        print() {
            var logging = "";
            for (var i = 0; i <= this.stack.length; i++) {
                if (this.stack[i]) {
                    logging += this.stack[i] + " ";
                }
            }
            console.log(logging);
        }
    }
    
    myStack = new arrStack();
    myStack.push(1);
    myStack.push(2);
    myStack.push(3);
    myStack.print();
    
    myStack.pop();
    myStack.print();
    
    console.log(myStack.top())
    
    // Given two Stack objects, create a standalone function to return whether they are equal. Stacks are equal only if they have equal elements in identical order. You can use an additional third Stack for storage; you will need it because you must return the given Stacks to their original condition upon exit. 
    
    
    ///var newStack =[]
    function compareStacks(stack1,stack2){
        if(stack1.length == stack2.length){
            for(i=0,i<stack1.length,i++){
                if(stack1[i] != stack2[i])
                    return false
            }
            return true 
        }
        return false    
    }


// Recursive Sigma
// Write a recursive function that given a number returns sum of integers from 1 to that
// number. Example: rSigma(5) = 15 (1+2+3+4+5); rSigma(2.5) = 3 (1+2); rSigma(-1) = 0.

function rSigma(sum, num) {
    num = Math.floor(num)
    if (num <= 0) {
        return console.log(sum);
    } 
    rSigma(sum += num, num - 1);
}

// Recursive Factorial
// Given num, return the product of ints from 1 up to num. If less than zero, treat as zero. If not integer, truncate. Experts tell us 0! is 1. rFact(3) = 6 (1*2*3). Also, rFact(6.5) = 720 (1*2*3*4*5*6).
    
function rFact(prd, num) {
    num = Math.floor(num)
    if ( num <=0) {
        return console.log(prd)
    }
    rFact(prd*=num, num - 1)
