# Optimization of production costs
In order to optimize production costs, the smelter decided to reduce electricity consumption during the steel processing stage.

**The goal of the project** is to build a model that will predict the final steel melting temperature.

**Stack:** `Pipeline` `Optuna` `pandas` `Catboost` `XGBoost`

## Conclusion
We have analyzed the process of steel melting, namely, information containing information about the electrodes, bulk materials (volume and time of supply), gas purge of the alloy, wire materials (volume and time), as well as the results of measuring the steel temperature.

When melting metal, the ladle is heated using electrodes, the heating power is determined by the power of the electrodes, which are characterized by active power, reflecting the process of converting electrical energy into heat (useful, real power) and reactive - a value that characterizes the loads created in electrical devices by fluctuations in the energy of the electromagnetic field in chains (side effect, losses).

Also, during the melting process, it is determined which substances are missing in order to obtain a certain steel grade, so loose and wire-like substances are added, which are stirred with gas. There are 15 bulk materials and 9 wire materials in total. There are many gaps in the data, since only some of the missing substances are added for a certain batch. Most often, Bulk 12, Bulk 14, Bulk 15, Wire 1 and Wire 2 are added, and least often - Bulk 2, Bulk 8, Bulk 9, Bulk 13, Wire 4, Wire 5 and Wire 7, which is due to the technological process (the difference in raw materials from which steel is made.

To train the model, data were prepared that included the initial measurement of the steel temperature, the final temperature of the steel, the time interval between the initial and final temperature measurements, the active and reactive power of the electrodes, the number of electrode heatings, the arc heating time, the volume of gas, and the volumes of various bulk and wire materials.

The best model for determining the final temperature of a batch of steel during melting is CatBoost with hyperparameters: `depth = 5, l2_leaf_reg = 4, learning_rate = 0.038, iterations = 1681, random_strength = 5`, which showed an average absolute deviation on the test sample of 5.77 degrees, which is good result.
