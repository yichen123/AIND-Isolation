##Chosen paper: Mastering the game of Go with deep neural networks and tree search

Go is the most challenging classic two-players perfect infomation games for the game tree searching. The game's breadth is around 250, and depth is around 150, which means fully searching a game tree for that game certainlly takes ages. 

For decades, AI researchers trying to use the reinforced learning to reduce the time for making actions. That is the computer will record actions and the game state, and update thier values based on the result. The most popular method before this paper is Monte Carlo tree search (MCTS). That is the AI simulating the game, and as the process goes on, the value of each action at specific game state will become accurate, and the policy will be able to sellect the moves with higher values. But result is not very good as the value funtion of this method is based on linear combination of the input features.


This paper is introducing the first method that implimenting the neural network into the game play to make the input feature more complex. When a neural network or so-called deep learing is given a move and game state as the input, the AI then uses multiple layers to decomposite and transform it. The network can extract certain feature from the input, and assign different values to certain features. Then it combines all these value  into one final value. As the result, the AI will be to assign a more reasonable value to the moves than the previous mehtod. The programme for demonstrate this method is called Alpha Go.

As the paper stated, after trained with huge amount of games, Alpha Go dominates the game against all the other Go programmes that based on the previous methods:

>"The results of the tournament suggest that singlemachine AlphaGo is many dan ranks stronger than any previous Go program, winning 494 out of 495 games (99.8%) against other Go programs. To provide a greater challenge to AlphaGo, we also played games with four handicap stones (that is, free moves for the opponent); AlphaGo won 77%, 86%, and 99% of handicap games against Crazy Stone, Zen and Pachi, respectively. The distributed version of AlphaGo was significantly stronger, winning 77% of games against single-machine AlphaGo and 100% of its games against other programs."

Alpha Go also beats the professional 2 Dan human player Fan Hui (see the Table below), which is a ground breaking achievement of AI.

![Details of match between AlphaGo and Fan Hui](http://ojjmxp9dc.bkt.clouddn.com/2017-08-25-%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-25%20%E4%B8%8A%E5%8D%8810.22.23.png)










