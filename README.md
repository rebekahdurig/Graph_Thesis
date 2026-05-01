# Graph_Thesis

##Previous Work
This is a recode of work done for my master's thesis, which was digging more deeply into work my advisor had previously done.
Original Paper: Harmonic Evolutions on Graphs by Jerzy Kocik (2012)
Original Thesis: The Game of Light: A Graph Theoretic Approach by Rebekah Durig (2017)

The code in my thesis was originally Java-based.

##This Code
This code was rewritten to accomplish several things:
1. I no longer code in Java and was looking for a way to improve my Python skills.
2. The code originally was tested up to 16 data points. It was highly accurate, but a 16 point graph was calculating for over 8 hours in ~2016 and didn't return a result. Based on my improved knowledge of packages since grad school, I knew there were ways to improve efficiency, and I found ways to improve my algorithm beyond working with a linear algebra package
3. My advisor had suggested adding a GUI to the original project. I had created a GUI, but had not been able to connect the GUI with the calculator. That now exists
4. I'm interested in pushing my code to understand if the original theorems work in Zp, not just Z2. This is still outstanding work, but I'm working on updating the GUI to accept other mods and visualize them, and then will start working on the math after the GUI can help with calculations

###Process
First, some of this program was vibe-coded in Claude. I explained the broad outline of what I wanted it to do, and was talking to it about options on how to code a GUI in Python, perhaps using Processing. Mots of my work in Python has been based around data/Pandas so far. I used Processing to code my original GUI, and it seemed like there may have been an update where it would support Python, but after some experimentation, that didn't seem like a good option. Claude ended up writing the basic structure of the GUI, but left a lot of the implementation to me.

My coding on this project included programming the rules that governed which nodes were on/off over time, as well as doing all coding related to the linear algebra of this problem: in particular the methods harmonic_matrix, mobius, calculate_gol, calculate_trees, calculate_loops. I may have added other methods as well. For example, I think there wasn't a delete_edges method in the original. I really enjoyed this workflow - it felt like collaboration with someone more experienced than I was in Python, and I was able to imitate some of the conventions/syntax to break down my testing.

One unexpected challenge was rewriting the Mobius function. This function seems like a relatively common number theory function, and I know I was able to get code for this function online for my thesis originally. When I was searching for an algorithm online, the ones I found were returning incorrect answers for fairly small numbers. After some trial and error, I decided to code the algorithm myself. In the debugging process, I gained a lot of nuance on why finding an efficient algorithm is tricky for this problem, and have identified a possible scenario where my current method will return incorrect answers for very large composite numbers. However, I think this is one place that I can improve, just thinking through the best way to do so.
