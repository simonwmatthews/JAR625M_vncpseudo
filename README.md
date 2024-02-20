# JAR625M Pseudosection Calculations

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/simonwmatthews/JAR625M_vncpseudo/HEAD)

## Instructions for loading the MAGEMin App

*The interface is often slow to respond- please be patient*

1. Click the Binder button above
2. If myBinder takes a long time to load, try refreshing the page
3. A screen will appear with several square buttons, click "Desktop"
4. A new tab will open. It will probably fail loading- refresh this page.
5. A desktop should appear
6. Click the terminal button on the bar at the bottom (second from the left)
7. Type "firefox" then press enter, a Firefox web browser window should open
8. Go back to the terminal, click on "File", then "New Tab"
9. Now type "julia" and press enter, it will take some time to load. Ignore the error messages
10. Once the prompt reads "julia>", type "using MAGEMinApp" and press enter. It will take some time to respond
11. Once the prompt reads "julia>" again, type App() and press enter. Wait for it to respond.
12. A message will appear saying "Listening on 127.0.0.1:8050"
13. Go back to Firefox and type "127.0.0.1:8050" in the address bar and press enter
14. An interface will appear, you are now ready to calculate pseudosections!

*You can also install MAGEMin directly onto your computer by following the instructions on the [MAGEMin website](https://github.com/ComputationalThermodynamics/MAGEMin/tree/main). You will need to install the [julia programming language](https://julialang.org) first*

## Exercise instructions

1. On the Thermodynamic Database choice pick one of the options based on the sort of rock you want to calculate. E.g., the igneous set for mantle melting, the metabasite set for metamorphosed basalts, the metapelite set for metamorphosed mudstones.
2. Choose a pressure and temperature range. Try to choose a realistic range for the rock type you chose, but you can always adjust it later.
3. In the central pane, you can choose from a set of rock compositions. You can also edit the proportions of different components- you might want to play with this after calculating one diagram.
4. Click the "Compute Phase Diagram" button on the right. Press this only once- otherwise the App will crash. It will appear not to be doing anything, but if you go back to the terminal window you will see a progress bar. The algorithm has to do many thousands of calculations to find the lowest Gibbs Free energy set of minerals.
5. Once the calculation is complete the view will switch to the "Phase Diagram" tab.
6. You should see a course pixelated map of mineral assemblages. Click "Grid Refinement" on the right hand side and wait again (see the terminal window for updates). It will start to calculate a finer grid, and will take some time as it has to do many calculations again.
7. You can keep on refining the grid if you want. Depending on the complexity of the diagram and the pressure and temperature range it might be fine after a single refinement.
8. Experiment with the plotting options on the right hand side. E.g., you can view the grid that the calculation has been run over (it will show a finer grid near reaction boundaries). You can also plot the entropy. If you click on a part of the diagram it will give you some more information about the phases at the pressure and temperature.
9. Click on the "Simulation" tab and adjust the inputs if you like.
