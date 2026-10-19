# Post-finish movement

Because the movement call follows the finish check inside each iteration, a turtle that triggers the finish condition can still receive its `forward(random.randint(0, 10))` call during that iteration. The loop stops on the next outer condition check.