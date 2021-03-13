# US 01.01.01 - Publish Experiment

As an owner, I want to publish an experiment with a description, a region, and a minimum number of trials.

## Story Points:

8

## Risk:

HIGH

## Rationale / Functionality:

1. User chooses to publish experiment
2. User is assigned to be the owner and must fill in the description, region, and minimum number of trial fields
3. Also to be considered: geolocation required, experiment trial type, etc.
4. Upon filling in these fields, the experiment becomes active

## Initial Associated GitHub Tasks:

- Create global experiment tracker
- User indication to create a new experiment (button, etc.)
- Fragment for new experiment; form must include necessary fields
- Experiment object creation and updating of viewable experiments, etc.

# US 01.02.01 - Unpublish Experiment

As an owner, I want to unpublish an experiment.

## Story Points:

2

## Risk:

HIGH

## Rationale / Functionality:

1. User indicates they want to unpublish an experiment; if they are the owner allow it
2. Remove the experiment from the active list (do not delete the data)

## Initial Associated GitHub Tasks:

- User indication to unpublish an experiment (UI element, maybe a button - maybe only viewable if they are the owner)
- Experiment object removal and updating of viewable experiments, etc.

# US 01.03.01 - End Experiment

As an owner, I want to end an experiment. This leaves the results available and public but does not allow new results to be added.

## Story Points:

5

## Risk:

MEDIUM

## Rationale / Functionality:

1. User indicates they want to end an experiment; if they are the owner allow it
2. Experiment moves from active to ended and trials can no longer be added, etc.

## Initial Associated GitHub Tasks:

- User indication to unpublish an experiment (UI element, maybe a button - maybe only viewable if they are the owner)
- Experiment object status update - move from active to ended list, disallow editing
- Disallow editing of this experiment

# US 01.04.01 - Subscribe to Experiment

As an owner or experimenter, I want to subscribe to an experiment to participate in it.

## Story Points:

3

## Risk:

LOW

## Rationale / Functionality:

1. Add this experiment to the user&#39;s subscription list (no effect on whether or not they can add trials, just for their own internal filtering)

## Initial Associated GitHub Tasks:

- User indication to subscribe to an experiment (UI element, maybe a visually updated toggle icon)
- Update list of subscribed-to experiments for this user

# US 01.05.01 - Execute Trials for Experiment

As an experimenter, I want to be able to execute trials for an experiment and upload them to the experiment.

## Story Points:

8

## Risk:

HIGH

## Rationale / Functionality:

1. User chooses to add a trial to an experiment
2. Upon filling in the data necessary to the experiment&#39;s associated trial type, user chooses to upload to experiment
3. Experiment data is updated to reflect this addition

## Initial Associated GitHub Tasks:

- User indication to execute a trial for an experiment (UI element, maybe a button)
- Fragment (different for each trial, geolocation requirements, etc.) to add a trial result to experiment
- Update experiment&#39;s data with user&#39;s entry
- A pop up screen of some sort indicating the details of which path the experiment is going to take

# US 01.06.01 - Trial Result Histograms

As an owner or experimenter, I want to see histograms of the results of trials.

## Story Points:

5

## Risk:

MEDIUM

## Rationale / Functionality:

1. User chooses to see a histogram-style view of trial results
2. Have the histogram up at all time to allow user to see the graphs on screen

## Initial Associated GitHub Tasks:

- UI construction of histogram that draws on Experiment&#39;s trials statistical data (depending on the experiment)

# US 01.07.01 - Trial Results Time Plots

As an owner or experimenter, I want to see plots of the results of trials over time.

## Story Points:

5

## Risk:

MEDIUM

## Rationale / Functionality:

1. User chooses to see a time-plot view of trial results

## Initial Associated GitHub Tasks:

- UI construction of time plots that draws on Experiment&#39;s trials statistical data

# US 01.08.01 - Ignore certain experiments

As an owner, I want to ignore certain experimenter&#39;s results.

## Story Points:

3

## Risk:

MEDIUM

## Rationale / Functionality:

1. An owner selects an experimenter to remove(ignore) from statistical consideration
2. All of that experimenter&#39;s results are ignored, a non-factor for that particular experiment

## Initial Associated GitHub Tasks:

- Owner tool to view experiment participants and select who&#39;s trial contributions to ignore
- Add participants to blacklist on a per-experiment basis
- Update that experiment&#39;s data set to reflect actual contributors vs ignored ones

# US 01.09.01 - Statistics View

As an owner or experimenter, I want to observe statistics (quartiles, median, mean, stdev) about current trials.

## Story Points:

3

## Risk:

MEDIUM

## Rationale / Functionality:

1. Each experiment has an option to view statistics (specified above) about the current trials

## Initial Associated GitHub Tasks:

- Create UI view accessible from experiment details that shows the specified statistic values