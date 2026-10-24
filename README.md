# CS370_CurrentTrends
What I Did on This Project

This project is a pirate NPC that learns to find treasure in an 8x8 maze using deep Q-learning, built in Python with TensorFlow and Keras.

What I was given: The starter notebook came with most of the supporting pieces. That included the maze environment (TreasureMaze), the experience replay class (GameExperience), the neural network builder, the play_game and completion_check functions, and the hyperparameters like epsilon, batch size, and memory size. I wasn’t allowed to modify the .py files, so everything I did lived in the notebook.

What I created: I wrote the Q-training loop inside the qtrain function. Each epoch, the pirate starts from a random free cell so it learns routes from anywhere in the maze, not just the top left. It picks actions with an epsilon-greedy rule, takes a step, stores the result in experience replay, and trains the model on a random batch from memory. I also added a periodic sync of the target network to keep training stable. With these settings, the pirate reached a 100% win rate at epoch 325, after about 7.8 minutes of training.

Connecting This to the Field of Computer Science

What do computer scientists do and why does it matter? Computer scientists turn real problems into systems that actually work. In this course, that meant taking a vague goal like “get the pirate to the treasure” and turning it into states, actions, rewards, and a training loop. It matters because software now touches money, health, and everyday decisions, so how we build it affects real people.

How do I approach a problem as a computer scientist? I break it into smaller pieces, figure out what I already have and what’s missing, and test as I go. This project showed me that even a working algorithm needs tuning and patience, since my first run threw an error that I had to track down before training could even start. I also learned to ask what the data and the rewards are really teaching the system, because an agent only learns what it’s rewarded for.

What are my ethical responsibilities to the end user and the organization? To users, I’m responsible for protecting their data, being transparent about how a system uses it, and making sure automated decisions are fair and can be explained. The GDPR principles from this course, like data minimization and purpose limitation, are a good checklist for that. To the organization, I’m responsible for being honest about what a model can and can’t do, documenting my work, and raising concerns early instead of letting a risky system ship. Working in compliance, I’ve seen that trust is hard to rebuild once it’s lost.
