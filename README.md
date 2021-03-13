# 01 - EXPERIMENT

## US 01.01.01 - Publish Experiment

As an owner, I want to publish an experiment with a description, a region, and a minimum number of trials.

### Story Points:

8

### Risk:

HIGH

### Rationale / Functionality:

1. User chooses to publish experiment
2. User is assigned to be the owner and must fill in the description, region, and minimum number of trial fields
3. Also to be considered: geolocation required, experiment trial type, etc.
4. Upon filling in these fields, the experiment becomes active

### Initial Associated GitHub Tasks:

- Create global experiment tracker
- User indication to create a new experiment (button, etc.)
- Fragment for new experiment; form must include necessary fields
- Experiment object creation and updating of viewable experiments, etc.

## US 01.02.01 - Unpublish Experiment

As an owner, I want to unpublish an experiment.

### Story Points:

2

### Risk:

HIGH

### Rationale / Functionality:

1. User indicates they want to unpublish an experiment; if they are the owner allow it
2. Remove the experiment from the active list (do not delete the data)

### Initial Associated GitHub Tasks:

- User indication to unpublish an experiment (UI element, maybe a button - maybe only viewable if they are the owner)
- Experiment object removal and updating of viewable experiments, etc.

## US 01.03.01 - End Experiment

As an owner, I want to end an experiment. This leaves the results available and public but does not allow new results to be added.

### Story Points:

5

### Risk:

MEDIUM

### Rationale / Functionality:

1. User indicates they want to end an experiment; if they are the owner allow it
2. Experiment moves from active to ended and trials can no longer be added, etc.

### Initial Associated GitHub Tasks:

- User indication to unpublish an experiment (UI element, maybe a button - maybe only viewable if they are the owner)
- Experiment object status update - move from active to ended list, disallow editing
- Disallow editing of this experiment

## US 01.04.01 - Subscribe to Experiment

As an owner or experimenter, I want to subscribe to an experiment to participate in it.

### Story Points:

3

### Risk:

LOW

### Rationale / Functionality:

1. Add this experiment to the user&#39;s subscription list (no effect on whether or not they can add trials, just for their own internal filtering)

### Initial Associated GitHub Tasks:

- User indication to subscribe to an experiment (UI element, maybe a visually updated toggle icon)
- Update list of subscribed-to experiments for this user

## US 01.05.01 - Execute Trials for Experiment

As an experimenter, I want to be able to execute trials for an experiment and upload them to the experiment.

### Story Points:

8

### Risk:

HIGH

### Rationale / Functionality:

1. User chooses to add a trial to an experiment
2. Upon filling in the data necessary to the experiment&#39;s associated trial type, user chooses to upload to experiment
3. Experiment data is updated to reflect this addition

### Initial Associated GitHub Tasks:

- User indication to execute a trial for an experiment (UI element, maybe a button)
- Fragment (different for each trial, geolocation requirements, etc.) to add a trial result to experiment
- Update experiment&#39;s data with user&#39;s entry
- A pop up screen of some sort indicating the details of which path the experiment is going to take

## US 01.06.01 - Trial Result Histograms

As an owner or experimenter, I want to see histograms of the results of trials.

### Story Points:

5

### Risk:

MEDIUM

### Rationale / Functionality:

1. User chooses to see a histogram-style view of trial results
2. Have the histogram up at all time to allow user to see the graphs on screen

### Initial Associated GitHub Tasks:

- UI construction of histogram that draws on Experiment&#39;s trials statistical data (depending on the experiment)

## US 01.07.01 - Trial Results Time Plots

As an owner or experimenter, I want to see plots of the results of trials over time.

### Story Points:

5

### Risk:

MEDIUM

### Rationale / Functionality:

1. User chooses to see a time-plot view of trial results

### Initial Associated GitHub Tasks:

- UI construction of time plots that draws on Experiment&#39;s trials statistical data

## US 01.08.01 - Ignore certain experiments

As an owner, I want to ignore certain experimenter&#39;s results.

### Story Points:

3

### Risk:

MEDIUM

### Rationale / Functionality:

1. An owner selects an experimenter to remove(ignore) from statistical consideration
2. All of that experimenter&#39;s results are ignored, a non-factor for that particular experiment

### Initial Associated GitHub Tasks:

- Owner tool to view experiment participants and select who&#39;s trial contributions to ignore
- Add participants to blacklist on a per-experiment basis
- Update that experiment&#39;s data set to reflect actual contributors vs ignored ones

## US 01.09.01 - Statistics View

As an owner or experimenter, I want to observe statistics (quartiles, median, mean, stdev) about current trials.

### Story Points:

3

### Risk:

MEDIUM

### Rationale / Functionality:

1. Each experiment has an option to view statistics (specified above) about the current trials

### Initial Associated GitHub Tasks:

- Create UI view accessible from experiment details that shows the specified statistic values

# 02 - QUESTIONS

## US 02.01.01 - Ask Question

As an experimenter, I want to ask a question about an experiment.

### Story Points:

2

### Risk:

LOW

### Rationale / Functionality:

1. Users have the option to ask questions in the experiment&#39;s forum-style chat area

### Initial Associated GitHub Tasks:

- Create UI element (maybe new question textbox) to ask a new question

- Update the experiment question area to show this new viewable, replyable entity
- Keep track of user, date, etc.

## US 02.02.01 - Reply to Questions

As an experimenter or owner, I want to ask to reply to questions about an experiment.

### Story Points:

3

### Risk:

LOW

### Rationale / Functionality:

1. Users have the option to reply to previously posted experiment questions (ask?)

### Initial Associated GitHub Tasks:

- Create UI element (maybe reply textbox) to add a question reply

- Update the experiment question area to show this new viewable reply

## US 02.03.01 - Reply to Questions

As an experimenter or owner, I want to browse questions and replies about an experiment.

### Story Points:

8

### Risk:

HIGH

### Rationale / Functionality:

1. Each experiment has an associated chat-style forum with questions and replies
2. Users can peruse the forum, and if they choose can post questions or replies

### Initial Associated GitHub Tasks:

- Create chat room view that is accessible from each experiment

- Allow posting of questions, responses to them, and update the view to reflect these user interactions

# 03 - QR CODES

## US 03.01.01 - Generate QR Code

As an experimenter, I want to be able to generate QR codes that I can print for a specific experiment and trial result (for instance PASS for a binomial trial I subscribed to).

### Story Points:

5

### Risk:

MEDIUM

### Rationale / Functionality:

1. User chooses to generate a QR code which represents a specific experiment/trial result combination

### Initial Associated GitHub Tasks:

- Create unique, viewable QR code based on experiment and trial result
- Allow printing of the QR code

## US 03.02.01 - Scan QR Code

As an experimenter, I want to be able scan QR codes to indicate success or failure, or increment counts for trials I subscribed to.

### Story Points:

8

### Risk:

MEDIUM

### Rationale / Functionality:

1. User scans a QR code
2. QR code applies a certain trial outcome to the subscribed experiment

### Initial Associated GitHub Tasks:

- Allow QR code integration; scanning applies that QR code&#39;s action to the experiment

## US 03.03.01 - Register Bar Code

As an experimenter, I want to be able to register an arbitrary bar code (such as one off of your favourite book) to act a specific experiment result for a trial.

### Story Points:

8

### Risk:

MEDIUM

### Rationale / Functionality:

1. User registers bar code to represent a specific trial/experiment result
2. Once scanned the bar code applies that action to the experiment

### Initial Associated GitHub Tasks:

- Register bar codes and their action under the associated experiment based on scanner
- If registered, apply the action and update experiment data when the bar code is scanned

# 04 - USER PROFILE

## US 04.01.01 - Profile with Unique Name

As an owner or experimenter, I want a profile with a unique username and my contact information.

### Story Points:

5

### Risk:

HIGH

### Rationale / Functionality:

1. Upon first-time startup user is assigned a unique id
2. User can optionally enter contact information into their profile

### Initial Associated GitHub Tasks:

- Create user object and first-time interaction behaviour

- Maintain referenceable list of app participants

## US 04.02.01 - Edit Profile Contact Information

As an owner or experimenter, I want to edit the contact information in my profile.

### Story Points:

1

### Risk:

MEDIUM

### Rationale / Functionality:

1. User can choose to edit all their contact information

### Initial Associated GitHub Tasks:

- Create fragment for a user to edit their own contact information

## US 04.03.01 - View User Profile

As an owner or experimenter, I want to retrieve and show the profile of a presented username.

### Story Points:

2

### Risk:

LOW

### Rationale / Functionality:

1. Based on selection (chat room, search, experiment participant list, etc.), show the user&#39;s profile

### Initial Associated GitHub Tasks:

- Create view (or fragment) for viewing a user&#39;s profile
- Be able to click on a profile from anywhere in the application

# 05 - SEARCHING

## US 05.01.01 - Search for Available Experiments

As an experimenter, I want to specify a keyword, and search for all experiments that are available.

### Story Points:

5

### Risk:

HIGH

### Rationale / Functionality:

1. User searches for a keyword (or/and toggles some sort of filter) to search for available experiments
2. Experiments are returned based the matched criteria for the user to view

### Initial Associated GitHub Tasks:

- Implement a basic search feature for experimenters

### BROKE INTO ADDITIONAL STORIES:

## US 05.03.01

## US 05.02.01 - Search Results Formatting

As an experimenter, I want search results to show each experiment with its description, owner username, and status.

### Story Points:

3

### Risk:

LOW

### Rationale / Functionality:

1. Based on user search results, show experiments matching the criteria
2. Show experiments in some kind of list format with description, owner username, and status

### Initial Associated GitHub Tasks:

- Set up a view to show each experiment&#39;s description, owner name, status after a user&#39;s search criteria

## US 05.03.01 - Custom Search / Filter List

As an experimenter, I want to be able to specify and filter by a number of options including geo-location required, owned, subscribed, popular, etc.

### Story Points:

8

### Risk:

LOW

### Rationale / Functionality:

1. User selects the search functionality
2. User can narrow and filter all experiments by a number of criteria that they can fine-tune or turn on and off; criteria may include various experiment stats, personal stats, experiment types or states, etc.

### Initial Associated GitHub Tasks:

- Implement a more advanced search feature for experiments

# 06 - LOCATION

## US 06.01.01 - Trial Geo-Location Required

As an owner, I want to specify if a Geo-location is required or not for trials.

### Story Points:

2

### Risk:

MEDIUM

### Rationale / Functionality:

1. When an experiment is being set up, owner must specify if a geo-location is required for all trials

### Initial Associated GitHub Tasks:

- Make sure some kind of toggle is implemented in the new experiment fragment and that the experiment is associated with this requirement

## US 06.02.01 - Add Geo-Location to Trials

As an experimenter, I want to add Geo-location to experimental trials that need it.

### Story Points:

5

### Risk:

MEDIUM

### Rationale / Functionality:

1. Upon uploading a trial, experimenters may need to add a geo-location
2. If the trial requires it, experimenters then add this information before uploading trial results

### Initial Associated GitHub Tasks:

- Ensure that if a trial requires geo-location information, the user is aware and adds this data upon upload (fragment or field?)
- User should be able to pin a point on a map, or search for a location

## US 06.03.01 - Geo-Location Warning

As an experimenter, I want to be warned about geo-location trials.

### Story Points:

1

### Risk:

LOW

### Rationale / Functionality:

1. If a experimenter will be required to upload their geo-location data in their trials, warn them

### Initial Associated GitHub Tasks:

- Ensure that experiments have geo-location as an attribute and that its visible or filterable somehow
- Create some kind of warning (maybe pop-up or some kind of indicator) to inform users when their trial is geo-location required

## US 06.04.01 - View Map of Geo-Locations

As an experimenter, I want to see a map of geo-locations of a geo-location enabled experiment.

### Story Points:

8

### Risk:

MEDIUM

### Rationale / Functionality:

1. In the experiment details, allow viewing of a map
2. Map shows geo-locations of submitted trials if it is enabled in the experiment

### Initial Associated GitHub Tasks:

- Create UI element (maybe button) to access experiment map
- Show all geo-location points on the map that users have submitted for that experiment