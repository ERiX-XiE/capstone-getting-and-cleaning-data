# capstone-getting-and-cleaning-data

My "run_analysis.R" file is already commented with quite detailed explanations about how it works, so here is only a brief version
When the working directory is set up to "~/UCI HAR Dataset", just run my_analysis_result() to get the output

The functions in run_analysis.R:
main functions:
%%%%%%%%% my_analysis_result(): to export the finished data set to the current working directory %%%%%%%%%

%%%%%%%%% my_analysis(): For steps 1~4 %%%%%%%%%

1.read and merge all 6 data files(subject、X、y files for train & test)
2.remove undesired columns, keep those about mean and std, as well as the "subject" and "activity" columns, with the aid of the helper function find_indices()
3.change "activity" values from integers to characters/strings, like number 1 should become "WALKING", 2 should be "WALKING_UPSTAIRS", with the aid of the helper function descriptive_act_names()
4.add descriptive names to the variables, with the aid of the helper function revised_variable_names()

######### my_analysis_2(): Especially for step 5 %%%%%%%%%

minor helper functions:
%%%%%%%%% find_indices(): %%%%%%%%%

locate the indices of the columns that are about mean and std, and return this list of indices in sorted order

%%%%%%%%% revised_variable_names(): %%%%%%%%%

minor changes to the original names of variables (not knowing if i should)
change 1: substitute _ for -
change 2: substitute [Bb]ody for [Bb]ody[Bb]ody occurrences because it seems repetitive

%%%%%%%%% descriptive_act_names(): %%%%%%%%%

convert a list of "activities values" from integers 1~6 to names in character, such as "WALKING", according to the activity_labels.txt file




