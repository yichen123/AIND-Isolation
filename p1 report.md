## Overall perfomance
![](http://ojjmxp9dc.bkt.clouddn.com/2017-08-16-%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-16%20%E4%B8%8B%E5%8D%889.16.34.png)

As we can see from above, the three score functions' result is just above the `AB_improved` winning rate, which is the benchmark of the test. I set game number between each set players to be `200`, for minizing the variation on winning rate.

###Custom 1
the score function I used in `custom 1` is

    player_moves - opponent_moves + 0.1 * player_distance_to_center

This function combines both `AB_improved` and `AB_open`. We put less weight on the distance since the perfomance of `AB_improved` is better than `AB_open`, also the scale of the distance is from 0~5, and we don't want it to be the dominating part. 

It turns out is slightly better than `AB_improved`, but not far ahead.



###Custom 2
The score function in `custom 2` is 

	players_moves - 2 * opponent_moves
	
This function is similar to `AB_improved`, but we put more weight on minimizing the opponent's available moves. Its perfomance is slight worse than `custom 1` and better than `AB_improved`.

###Custom 3
The score funtion I used in `custom 3` is 

	min(player_moves - opponent_moves, player_distance_to_center)
	
This function is another comination of `AB_improved` and `AB_open`. It turns out is slightly worse than `AB improved`.


##Conclusion

For computation complex, `AB_custom 2` clearly is the easiest funtion to compute, and then the `AB_custom 3`. The other two `AB_improved` and `AB_custom 1` are the more difficulty funtions to compute as they involve square and square roots. But on the other hand, they all just functions envlove only constants, which means they are the same when considering level of computational complex. As the result, they will go into the similar depth of the game tree.


![](http://ojjmxp9dc.bkt.clouddn.com/2017-08-25-%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-25%20%E4%B8%8B%E5%8D%882.29.32.png)

For the winning rate, we can see from above, our `AB_custom 1` has the best performance.

To conclude, I would recommond `AB_custom 1` here. As it has the best performance result, with the similar complex level as the other heuristic funcitons.





