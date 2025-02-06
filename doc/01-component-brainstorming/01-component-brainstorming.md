# Portfolio Part 1: Component Brainstorming

- **Name**: Meghana Boda
- **Dot Number**: Boda.21
- **Due Date**: 02/05/2025 @3pm

## Assignment Overview


The overall goal of the portfolio project is to have you design and implement
your own OSU component. There are no limits to what you choose to design and
implement, but your component must fit within the constraints of our software
sequence discipline. In other words, the component must extend from Standard and
must include both a kernel and a secondary interface.

Because this is a daunting project, we will be providing you with a series of
activities to aid in your design decisions. For example, the point of this
assignment is to help you brainstorm a few possible components and get some
feedback. For each of these components, you will need to specify the high-level
design in terms of the software sequence discipline. In other words, you will
describe a component, select a few kernel methods for your component, and select
a few secondary methods to layer on top of your kernel methods.

You are not required to specify contracts at this time. However, you are welcome
to be as detailed as you'd like. More detail means you will be able to get more
detailed feedback, which may help you decide which component to ultimately
implement.

## Assignment Checklist


To be sure you have completed everything on this assignment, we have littered
this document with TODO comments. You can browse all of them in VSCode by
opening the TODOs window from the sidebar. The icon looks like a tree and will
likely have a large number next to it indicating the number of TODOS. You'll
chip away at that number over the course of the semester. However, if you'd
like to remove this number, you can disable it by removing the following
line from the `settings.json` file:

```json
"todo-tree.general.showActivityBarBadge": true,
```

Which is not to be confused with the following setting that adds the counts
to the tree diagram (you may remove this one as well):

```json
"todo-tree.tree.showCountsInTree": true,
```

## Assignment Learning Objectives


Without learning objectives, there really is no clear reason why a particular
assessment or activity exists. Therefore, to be completely transparent, here is
what we're hoping you will learn through this particular aspect of the portfolio
project. Specifically, students should be able to:

1. Integrate their areas of interest in their personal lives and/or careers with
   their knowledge of software design
2. Determine the achievablility of a software design given time constraints
3. Design high-level software components following the software sequence
   discipline

## Assignment Rubric: 10 Points


Again, to be completely transparent, most of the portfolio project, except the
final submission, is designed as a formative assessment. Formative assessments
are meant to provide ongoing feedback in the learning process. Therefore,
the rubric is designed to assess the learning objectives *directly* in a way
that is low stakes—meaning you shouldn't have to worry about the grade. Just
do good work.

| Learning Objective                                                                                        | Subcategory                 | Weight | Missing                                                     | Beginning                                                                              | Developing                                                                                     | Meeting                                                                                 |
| --------------------------------------------------------------------------------------------------------- | --------------------------- | ------ | ----------------------------------------------------------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Students should be able to identify their values, interests, and/or goals as they relate to their designs | Metacognitive Memory        | 3      | (0) No attempt to summarize values, interests, and/or goals | (1) A brief description of values, interests, and/or goals is provided but lacks depth | (2) A description of values, interests, and/or goals is provided by are not related to designs | (3) A description of values, interests, and/or goals is provided and relates to designs |
| Students should be able to predict the feasibility of their designs                                       | Metacognitive Understanding | 3      | (0) No attempt to design components that are feasible       | (1) At least one component is feasible                                                 | (2) At least two components are feasible                                                       | (3) All three components are feasible                                                   |
| Students should be able to use the OSU discipline in all three designs                                    | Metacognitive Application   | 4      | (0) No attempt to follow the OSU discipline in designs      | (1) At least one design follows the OSU discipline                                     | (3) At least two designs follow the OSU discipline                                             | (4) All three designs follow the OSU discipline                                         |

Below is further rationale/explanation for the rubric items above:

1. Each design must align with your personal values and long-term
   goals. Because the goal of this project is to help your build out a
   portfolio, you really ought to care about what you're designing. We'll give
   you a chance to share your personal values, interests, and long-term goals
   below.
2. Each design must be achievable over the course of a single
   semester. Don't be afraid to design something very small. There is no shame
   in keeping it simple.
3. Each design must fit within the software sequence discipline. In
   other words, your design should expect to inherit from Standard, and it
   should contain both kernel and secondary methods. Also, null and aliasing
   must be avoided, when possible. The methods themselves must also be in
   justifiable locations, such as kernel or secondary.

## Pre-Assignment

> Before you jump in, we want you to take a moment to share your interests
> below. Use this space to talk about your career goals as well as your personal
> hobbies. These will help you clarify your values before you start
> brainstorming. Plus it helps us get to know you better! Feel free to share
> images in this section.

In my freetime, I love to explore music and dance. I'm extremely interested in the arts even though that may not be something I'd like to pursue as a career. However, I'd love to have a part time job as a dance teacher as I grow older. In the academic space, I'm passionate about machine learning and cybersecurity to contribute to a better society. Outside of that, I absolutely love binging a good show or watching movies and traveling is one of my favorite things today. Beach locations are some of my favorite spots and I also love the mountains.

## Assignment


As previously stated, you are tasked with brainstorming 3 possible components.
To aid you in this process, we have provided [some example components][example-components]
that may help you in your brainstorming. All of these components were made at
some point by one of your peers, so you should feel confident that you can
accomplish any of them.


There is no requirement that you use any of the components listed above.
If you want to model something else, go for it! Very common early object
projects usually attempt to model real-world systems like banks, cars,
etc. Make of this whatever seems interesting to you, and keep in mind that
you're just brainstorming right now. You do not have to commit to anything.

### Example Component


To help you brainstorm a few components, we've provided an example below of a
component you already know well: NaturalNumber. We highly recommend that you
mirror the formatting as close as possible in your designs. By following this
format, we can be more confident that your designs will be possible.

- Example Component: `NaturalNumber`
  - **Description**:
    - The purpose of this component is to model a non-negative
      integer. Our intent with this design was to keep a simple kernel that
      provides the minimum functionality needed to represent a natural number.
      Then, we provide more complex mathematical operations in the secondary
      interface.
  - **Kernel Methods**:
    - `void multiplyBy10(int k)`: multiplies `this` by 10 and adds `k`
    - `int divideBy10()`: divides `this` by 10 and reports the remainder
    - `boolean isZero()`: reports whether `this` is zero
  - **Secondary Methods**:
    - `void add(NaturalNumber n)`: adds `n` to `this`
    - `void subtract(NaturalNumber n)`: subtracts `n` from `this`
    - `void multiply(NaturalNumber n)`: multiplies `this` by `n`
    - `NaturalNumber divide(NaturalNumber n)`: divides `this` by `n`, returning
      the remainder
    - ...
  - **Additional Considerations** (*note*: "I don't know" is an acceptable
    answer for each of the following questions):
    - Would this component be mutable? Answer and explain:
      - Yes, basically all OSU components have to be mutable as long as they
        inherit from Standard. `clear`, `newInstance`, and `transferFrom` all
        mutate `this`.
    - Would this component rely on any internal classes (e.g., `Map.Pair`)?
      Answer and explain:
      - No. All methods work with integers or other NaturalNumbers.
    - Would this component need any enums or constants (e.g.,
      `Program.Instruction`)? Answer and explain:
      - Yes. NaturalNumber is base 10, and we track that in a constant called
          `RADIX`.
    - Can you implement your secondary methods using your kernel methods?
      Answer, explain, and give at least one example:
      - Yes. The kernel methods `multiplyBy10` and `divideBy10` can be used to
        manipulate our natural number as needed. For example, to implement
        `increment`, we can trim the last digit off with `divideBy10`, add 1 to
        it, verify that the digit hasn't overflown, and multiply the digit back.
        If the digit overflows, we reset it to zero and recursively call
        `increment`.

Keep in mind that the general idea when putting together these layered designs
is to put the minimal implementation in the kernel. In this case, the kernel is
only responsible for manipulating a digit at a time in the number. The secondary
methods use these manipulations to perform more complex operations like
adding two numbers together.

Also, keep in mind that we don't know the underlying implementation. It would be
completely reasonable to create a `NaturalNumber1L` class which layers the
kernel on top of the existing `BigInteger` class in Java. It would also be
reasonable to implement `NaturalNumber2` on top of `String` as seen in
Project 2. Do not worry about your implementations at this time.

On top of everything above, there is no expectation that you have a perfect
design. Part of the goal of this project is to have you actually use your
component once it's implemented to do something interesting. At which point, you
will likely refine your design to make your implementation easier to use.

### Component Designs

> Please use this section to share your designs.

- Component Design #1: Task Manager
  - **Description**:
    - The purpose of this component is to model the organization and management of to-do lists. It allows to manage tasks based on priority, deadline, or status and helps users manage tasks efficiently.
  - **Kernel Methods**:
    - `void addTask(Task t)`: adds a new task to the task manager
    - `void removeTask(Task t)`: removes a task from the task manager
    - `boolean isEmpty()`: checks if there are any tasks in the task manager
    - `Task getTaskAt(int index)`: retrieves a task at a specific index in the task manager
    - `void changeStatus(Task t, String status)`: updates the status of the task to complete or incomplete
  - **Secondary Methods**:
    - `void sortByPriority()`: sorts the tasks by their priority (e.g., high, medium, low)
    - `void sortByDeadline()`: sorts the tasks by their deadline date
    - `void sortByStatus()`: sorts the tasks by their status (e.g., pending, in progress, completed)
    - `List<Task> getTasksByStatus(String status)`: retrieves a list of tasks with a specific status
    - `Task searchByTitle(String title)`: searches for a task by its title
    - `List<Task> getOverdueTasks()`: retrieves a list of tasks that have missed their deadline
  - **Additional Considerations** (*note*: "I don't know" is an acceptable
    answer for each of the following questions):
    - Would this component be mutable? Answer and explain:
      - Yes, the task manager will be getting updated as tasks are getting added, removed, completed, and sorted.
    - Would this component rely on any internal classes (e.g., `Map.Pair`)?
      Answer and explain:
      - I don't think so.
    - Would this component need any enums or constants (e.g.,
      `Program.Instruction`)? Answer and explain:
      - The component would benefit from using enums for the Status (e.g., PENDING, IN_PROGRESS, COMPLETED) and Priority (e.g., HIGH, MEDIUM, LOW) of tasks. These enums provide better organization, validation, and readability, helping ensure tasks are in the correct state and can be easily sorted.
    - Can you implement your secondary methods using your kernel methods?
      Answer, explain, and give at least one example:
      - Yes. For example, searchByTitle(String title) could use a while loop and loop through all the elements and use the getTaskAt method once it finds the correct one.

- Component Design #2: Music Playlist
  - **Description**:
    - The purpose of this component is to model the organization of songs in a playlist. The intent of the design is to keep an ordered list of songs with basic operations to manage the playlist.
  - **Kernel Methods**:
    - `void addSong(Song s)`: adds a song to the playlist
    - `void removeSong(Song s)`: removes a song to the playlist
    - `void playNext()`: removes a song from the playlist
    - `void skip()`: skips the current song and moves to the next one
    - `boolean isEmpty()`: checks if the playlist is empty
  - **Secondary Methods**:
    - `void moveSong(int fromIndex, int toIndex)`: moves a song from one position to another in the playlist
    - `Song getSongAt(int index)`: retrieves the song at a specific index
    - `void shuffle()`: shuffles the order of the playlist
    - `int getTotalDuration()`: returns the total duration of all songs in the playlist
    - `void playSongAt(int index)`: plays a specific song at a given index
  - **Additional Considerations** (*note*: "I don't know" is an acceptable
    answer for each of the following questions):
    - Would this component be mutable? Answer and explain:
      - Yes, it is meant to change as songs are added, removed, rearranged, etc., modifying the state of the playlist
    - Would this component rely on any internal classes (e.g., `Map.Pair`)?
      Answer and explain:
      - I think it wouldn't but I'm not completely sure right now
    - Would this component need any enums or constants (e.g.,
      `Program.Instruction`)? Answer and explain:
      - No, it's pretty straightforward
    - Can you implement your secondary methods using your kernel methods?
      Answer, explain, and give at least one example:
      - Yes, many of the secondary methods can be implemented
using the kernel methods. The method moveSong(int fromIndex, int toIndex) could be implemented by first removing the song at fromIndex using removeSong() and then adding it back at toIndex using addSong(). Similarly, shuffle() can be implemented by repeatedly calling removeSong() and addSong() in a random order.

- Component Design #3: Data Analysis Dashboard
  - **Description**:
    - The Data Analysis Dashboard component models an interactive dashboard for analyzing various data sources. It allows users to load datasets, apply transformations, calculate summary stats, and visualize trends.
  - **Kernel Methods**:
    - `void loadData(String datasetName, List<DataPoint> data)`: loads a new dataset into the dashboard
    - `void applyTransformation(String transformationType)`: applies a specific transformation to the data (e.g., normalization, scaling, or filtering)
    - `double calculateMean(String column)`: calculates the mean of a given column in the dataset
    - `double calculateMedian(String column)`: calculates the median of a given column
    - `double calculateStandardDeviation(String column)`: calculates the standard deviation for a given column
    - `List<String> getColumnNames()`: returns the column names in the dataset
  - **Secondary Methods**:
    - `List<Double> plotHistogram(String column)`: generates a histogram of a specified column's data to analyze the distribution
    - `double calculateCorrelation(String column1, String column2)`: calculates the correlation between two columns in the dataset
    - `double calculateSkewness(String column)`: calculates the skewness of a column to understand its distribution
    - `List<String> filterData(String column, String condition)`: filters data based on a condition applied to a specific column (e.g., "greater than 50")
    - `String getTopPerformingCategory(String column)`: identifies and returns the category with the highest average value in a given column
    - `void createPivotTable(String rowColumn, String aggColumn)`: generates a pivot table by aggregating data based on rows and columns (e.g., sum, average)
  - **Additional Considerations** (*note*: "I don't know" is an acceptable
    answer for each of the following questions):
    - Would this component be mutable? Answer and explain:
      - Yes, the component would allow users to load new datasets, apply transoformations, etc.
    - Would this component rely on any internal classes (e.g., `Map.Pair`)?
      Answer and explain:
      - Potentially a Map<String, List> might be used to store the columns and their corresponding values for efficient access and manipulation
    - Would this component need any enums or constants (e.g.,
      `Program.Instruction`)? Answer and explain:
      - I think so but not sure yet
    - Can you implement your secondary methods using your kernel methods?
      Answer, explain, and give at least one example:
      - Yes, plotHistogram(String column) can leverage calculateMean() and calculateStandardDeviation() to plot relevant data points

## Post-Assignment

The following sections detail everything that you should do once you've
completed the assignment.

### Changelog


At the end of every assignment, you should update the
[CHANGELOG.md](../../CHANGELOG.md) file found in the root of the project folder.
Since this is likely the first time you've done this, we would recommend
browsing the existing file. It includes all of the changes made to the portfolio
project template. When you're ready, you should delete this file and start your
own. Here's what I would expect to see at the minimum:

```markdown
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Calendar Versioning](https://calver.org/) of
the following form: YYYY.0M.0D.

## YYYY.MM.DD

### Added

- Designed a <!-- insert name of component 1 here --> component
- Designed a <!-- insert name of component 2 here --> component
- Designed a <!-- insert name of component 3 here --> component
```

Here `YYYY.MM.DD` would be the date of your submission, such as 2024.04.21.

You may notice that things are nicely linked in the root CHANGELOG. If you'd
like to accomplish that, you will need to make GitHub releases after each pull
request merge (or at least tag your commits). This is not required.

In the future, the CHANGELOG will be used to document changes in your
designs, so we can gauge your progress. Please keep it updated at each stage
of development.

### Submission

<!-- TODO: read the submission instructions then delete this comment -->

If you have completed the assignment using this template, we recommend that
you convert it to a PDF before submission. If you're not sure how, check out
this [Markdown to PDF guide][markdown-to-pdf-guide]. However, PDFs should be
created for you automatically every time you save, so just double check that
all your work is there before submitting. For future assignments, you will
just be submitting a link to a pull request. This will be the only time
you have to submit any PDFs.

<!-- TODO: upload a PDF of this document and the CHANGELOG to Carmen then delete this comment -->

### Peer Review

<!-- TODO: review the peer review guidelines then delete this comment -->

Following the completion of this assignment, you will be assigned three
students' component brainstorming assignments for review. Your job during the
peer review process is to help your peers flesh out their designs. Specifically,
you should be helping them determine which of their designs would be most
practical to complete this semester. When reviewing your peers' assignments,
please treat them with respect. Note also that we can see your comments, which
could help your case if you're looking to become a grader. Ultimately, we
recommend using the following feedback rubric to ensure that your feedback is
both helpful and respectful (you may want to render the markdown as HTML or a
PDF to read this rubric as a table).

| Criteria of Constructive Feedback | Missing                                                                                                                           | Developing                                                                                                                                                                                                                                | Meeting                                                                                                                                                               |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Specific                          | All feedback is general (not specific)                                                                                            | Some (but not all) feedback is specific and some examples may be provided.                                                                                                                                                                | All feedback is specific, with examples provided where possible                                                                                                       |
| Actionable                        | None of the feedback provides actionable items or suggestions for improvement                                                     | Some feedback provides suggestions for improvement, while some do not                                                                                                                                                                     | All (or nearly all) feedback is actionable; most criticisms are followed by suggestions for improvement                                                               |
| Prioritized                       | Feedback provides only major or minor concerns, but not both. Major and minar concerns are not labeled or feedback is unorganized | Feedback provides both major and minor concerns, but it is not clear which is which and/or the feedback is not as well organized as it could be                                                                                           | Feedback clearly labels major and minor concerns. Feedback is organized in a way that allows the reader to easily understand which points to prioritize in a revision |
| Balanced                          | Feedback describes either strengths or areas of improvement, but not both                                                         | Feedback describes both strengths and areas for improvement, but it is more heavily weighted towards one or the other, and/or descusses both but does not clearly identify which part of the feedback is a strength/area for improvement  | Feedback provides balanced discussion of the document's strengths and areas for improvement. It is clear which piece of feedback is which                             |
| Tactful                           | Overall tone and language are not appropriate (e.g., not considerate, could be interpreted as personal criticism or attack)       | Overall feedback tone and language are general positive, tactul, and non-threatening, but one or more feedback comments could be interpretted as not tactful and/or feedback leans toward personal criticism, not focused on the document | Feedback tone and language are positive, tactful, and non-threatening. Feedback addesses the document, not the writer                                                 |

### Assignment Feedback

If you'd like to give feedback for this assignment (or any assignment, really),
make use of [this survey][survey]. Your feedback helps make assignments
better for future students.

<!-- TODO: follow the link to share your feedback then delete this comment -->

[example-components]: https://therenegadecoder.com/code/the-never-ending-list-of-small-programming-project-ideas/
[markdown-to-pdf-guide]: https://therenegadecoder.com/blog/how-to-convert-markdown-to-a-pdf-3-quick-solutions/
[survey]: https://forms.gle/dumXHo6A4Enucdkq9
