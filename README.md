# CodeExercise03

Hi there, welcome to Eulith. My name is Lucas, I'm a founder along with Moh and Kristian.

If you're reading this, you're most likely thinking about working with us as a back-end engineer. 
You no doubt have many alternatives; we deeply appreciate you considering us. 

The below describes a code exercise we give to potential back-end engineers. 
Our main evaluation criteria (other than assessing the first month of progress when you join) 
is how you do on the coding exercise. 

**When you read this, create a public repo (just with your own github account) and please send us the link to that public repo. You will keep your solution in this public repo.**

I think it's important to first highlight the "dimensions" on which we're going to be evaluating your solution:

**1) The work itself.**
We care about a few things:

- Your code quality: This should go without saying; if you submit a repo that's disorganized, hard to understand,
  contains files that shouldn't be in source control, etc, that's bad. We'll consider the benefits and
  limitations of your design.
- Shipping code that actually works: If you can't complete the whole task, you're better off shipping
  a smaller piece that works instead of just random code here and there that's supposed to show "intentions."
- Dependency decisions: We're going to think about your choice of libraries (if you used any)
  if this was a PR, what would need to change for us to confidently merge it into our codebase.
  We care about how the code is presented, whether it handles reasonable edge cases, whether
  it's robust, whether it's extendable.

**2) The time you spend on the exersice.**
The start time is when you create the public repo mentioned above. You're free to take as long as you want. We suggest 
you start immediately, but we don't expect you to finish it in 1 sitting (although you can if you want). 
We'll look at your Github commits and expect you to commit with a certain regularity (i.e. no single 
commit answers). We view the time you spend as an indication of your interest and work ethic 
(which we care a lot about). We also view your time spent as a variable of productivity. 
So there's some "optimization" here where you want to spend enough time to indicate a high work ethic, 
but not so much time relative to your output that your productivity/hour is low - honestly you 
shouldn't even worry about this and just do the task for as long as you feel appropriate; 
the explanation is only to give context.

**3) Your questions and explanations.**
Treat this like you're already working on our team. Naturally, you will have questions 
and we'll want to understand your approach/implementation. As usual, include any comments in your code
you think will be necessary for us to easily understand your approach. 
Write your broader explanations that would typically be a conversation 
in your README. Write your questions in your README (this is part of the submission). 
Provide context, but try to be _both precise and concise_ about the issue(s), 
particularly in your questions.

This is exercise is associated with this JD, in case the additional context helps 
(it's totally fine if you don't meet all the requirements, this is just for context): 
https://docs.google.com/document/d/13xf1_aaAMdrxoPxtE0k7-mEwwbh5b66nNy-bG_RAXN8/edit?usp=sharing 


Alright! Enough chit-chat. Here it is.

---

NOTE: ALL OF THIS SHOULD BE DEPLOYED ON A LOCAL CHAIN. YOU DON'T NEED TO USE REAL-WORLD ASSETS OR ETH FOR ANY OF THIS.

**Step 1**: Define a solidity contract that performs some function on-chain. What the function does is entirely up to you. We're leaving this intentionally "vague" because it's not so important what you pick. For example you could pick any one of these: 

1. Call a function to mutate the state of a string or struct
2. Call a function to mutate an integer. 
3. Call a function to send ETH to the contract.
4. Call a function to send ERC20 tokens to the contract.

Note all of these functions are on-chain. These are written in your contract. Do whatever you want here; the specific action isn't that important.

**Step 2**: Create a CLI that allows the user to:

1. Deploy your contract TO A LOCAL CHAIN (again, not real ETH). 
2. Monitor the results of the action from Step 1
3. Reset the contract to a neutral state (the state before the action)

**Step 3**: Write a Rust program that asynchronously monitors the contract in a non-blocking loop. Hint: you can either use OS threads or green threads
in a runtime like Tokio. When the state of your contract satisfies a constraint, take an action (like printing the satisfied state) and close the program
(including properly handling the shutdown of your parallel threads).

For example, the main thread of your program should deploy and set up the contract. Spawn a parallel thread to monitor for a certain condition.
Back in the main thread, take an action to satisfy the condition. Then acknowledge to the user that the condition was met, reset the 
contract state, and shut down the program.

---

Just message me if you have any questions, tg: luca590.

When you finish, email the public repo link to: team@eulith.com 
with the subject line: "CodeExercise02 Submission".

Thank you so much for taking the time out to do this assignment. 
We know it's a big time investment and really appreciate your willingness.


## FAQ
...
