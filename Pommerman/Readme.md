# Enhancement in Pommmerman MCTS Agent with Opponent Modelling

Monte Carlo Tree Search (MCTS) is the most widely used algorithm these days for real time games. This technique is used in pommerman for providing greater efficiency against other opponent (such as Simple Player, OSLA Player, RHEA Player). We have used the concept of opponent modelling to provide better competency against other players in pommerman. 

# Pommerman

The test platform of this game is created by GAIGResearch - (java-pommerman)[https://github.com/GAIGResearch/java-pommerman], and the method to install game can be found under that repositories.

# Agent

The GroupI file contains an Opponent Model Agent implemented in original MCTS Agent. Here we are using opponent Modelling technique where the agent can make prediction of it's behaviour by analysing the strategy of the opponent.

# Agent Implementation

To implement GroupI folder put it under src folder. To run the code add the following lines of code to Run.java and Test.java along with importing their classes:

Run.java:

                        MCTSParams mctsParams1 = new MCTSParams();
                        mctsParams1.stop_type = mctsParams1.STOP_ITERATIONS;
                        mctsParams1.num_iterations = 200;
                        mctsParams1.rollout_depth = 12;

                        mctsParams1.heuristic_method = mctsParams1.CUSTOM_HEURISTIC;
                        p = new NewMCTSPlayer(seed, playerID++, mctsParams1);
                        playerStr[i-4] = "NewMCTSPlayer";

Test.java:

                        players.add(new NewMCTSPlayer(seed, playerID++,mctsParams));

# Result

A significant improvement is seen by implementing opponent model with MCTS which result are shown in our report.