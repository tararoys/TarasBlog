Title: Threaded Servers Vs. Evented Servers, or the Bank Teller Vs. The Gossipy Neighbor
Author: Tara Roys
Date: Wed Mar 20 2013 10:16:51 GMT-0600 (CST)
Node: v0.1.102


I never really got the difference between a threaded server and an evented server until I likened a thread to a bank teller and an event loop to a gossipy neighbor.  Read on for the intricate analogy!

##Threaded Servers

A threaded server is like a bank.  When you walk in the front door of the bank, you immediately see a bank teller smiling at you.  You walk up to the teller, and tell her that you want to withdraw a hundred dollars from your bank account.  She smiles and says "wait one minute" and goes off and does what you ask. You notice that while she's gone, a line has formed behind you.   A few minutes later, she comes back with your money.  You leave, and she starts helping the next person in line.  

In this analogy, you are a request to the server.  The front door of the bank is a port.  The bank teller is a thread, and her job is to do what you request: in this case, giving you a hundred dollars.   The people behind you, waiting in line, are other requests.   Since the teller cannot help them until she finishes helping you, they are blocked, and they have to wait until you are done with the teller.  When people talk about blocking servers, this is what they mean:  people waiting in line until the teller can get around to helping them.  

The challenge of threaded servers is getting them to serve more than one request at once  A bank does this by hiring more tellers.  A multi-threaded server is basically doing the same thing: when several requests come it at once, it passes each request off to it's own thread, just like a bank would have a different teller handle each person in line.  

#Evented Servers:  

An evented server is like a gated community.  In this gated community is an old woman who spies on everybody and gossips about it to absolutely everyone.  The strange thing about this woman is that she's fast: her gossip seems to spread at the speed of light. People in the neighborhood learned to listen to the old woman for specific things they are interested in, and tune out the rest of her chatter.  Mr. Atwood, for example, is interested in knowing whenever a new car drives up to the front gate, because they are probably there to buy some of the drugs he's selling.  Whenever he hears that there's a car at the gate, he sends one of his dealers out to the car to make the sale.  Sometimes, there are several cars at the gate at once.  The old lady will talk about each one as it arrives, and Mr. Atwood will send a dealer to each one as it arrives.  There is no waiting in line:  because the old woman keeps Mr. Atwood informed, he can send a dealer out to make each sale immediately.

In this analogy, the car is a request to the server.  The old woman is called an event loop, and like the old lady, the even loop's job is to watch everything that happens on the server and talk about it.  From the event loops perspective, an event happened:  a car drove up to the front gate: and the event loop must tell everyone on the server about it.  Mr. Atwood is an event listener: his job is to listen for a specific thing in the event loop to happen.  In this case, he's listening for requests to the server, aka cars driving up to the front gate.  When he hears the event that he's listening for, he springs into action and sends a drug dealer to the car to make a sale.  The action that he takes is called a callback function.  A callback function is a function that is triggered by something happening: in this case, a car drives up, and that triggers a drug dealer being sent out to meet it.  

  An evented server can handle lots of requests at once.  In our neighborhood, no cars have to wait in line because the nosy old woman is so quick at telling Mr. Atwood about their arrival, and Mr. Atwood has an unlimited supply of drug dealers and can send one out to every car as it arrives.  
  

##Threaded vs. Evented Servers

The biggest practical difference between threaded and evented servers is how they deal with multiple requests at once.  Like a bank hiring more tellers, a threaded server's solution is to get more threads.  However, most banks have a limited amount of space where they can put more tellers.  Each teller needs a booth, and a computer, and there are only so many booths and computers to go around.  Likewise, many servers have a thread pool of about twenty threads. In short, a threaded server with a thread pool of twenty means that they can handle twenty threads at once, which is not so great if they get hit with a hundred or a thousand requests. 

 The biggest drawback of threaded servers is that once a thread is busy, it won't even notice when a new request arrives, and can't make smart decisions about who to serve first.  For example, say that at our bank the first person in line is a customer who needs to refinance their house, a process that takes hours.  The second person in line needs to check their balance, a process that takes 30 seconds.  The teller will choose the first person in line regardless of how long it would take.  It is strictly first-come, first-serve.  

Evented servers, on the other hand, rely on one event loop to decide what to do.  The event loop's only job is to notice when things happen and tell the rest of the server about it as quickly as possible, like our nosy old woman. In the [neighborhood.  Going back to our neighborhood analogy, let's say that a car drives up that wants to negotiate a particularly tricky crack deal, a process taking hours.  The event loop doesn't care:  she is a nosy old woman  who just says "The car is HERE!" and lets someone else deal with doing something about the car.  The next car in line just wants a dime bag, something that takes maybe ten seconds.  She doesn't care. She just says "The CAR IS HERE" and let's someone else take care of dealing with it.  Because the server quickly informed of all the requests as they come in, appropriate processes on the server are delegated to deal with them.  In our neighborhood analogy, this would result in the dime-bag car getting sent on his way much faster than the crack car.  



  
