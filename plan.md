### Plan

#### Task
* Build a dashboard that can be used to track metrics that measure the quality of the Questions & Answers user experience (UX)

#### Product Metrics
* The overall success is measured by a user experience methodology called HEART
* Heart stands for **Happiness**, **Engagement**, **Adoption**, **Retention** and **Task Success**

#### Tables and sub-tables inside the Database
Below is an assumption of what data we could find in the tables. Will need to look at it for real myself to understand better what the exact post types etc. are but this gives me a rough idea what I could be finding.
* **Users**: user information
    * *Users*: individual user info with creation date, no of views, email, display name etc.
    * *Badges*: badges that users can have base on ranking on stackoverflow i.e. bronze, silver, gold linking to their user id
* **Posts**: posts information 
    * *Posts*: individual post info with creation date, deletion date, score, views, a parent id which links to a parent post (if applicable) etc.
    * *PostNotices*: type of notice for the posts with post id attached. the notice could be a notification post from a owner or a forum discussion on an open ended question. info included are creation date, body (text of the post), name (headline of the post).
    * *PostNoticeTypes*: a table that records info to remind post owners to accept or reject an answer. there is a column (PostNoticeDurationId) where it could be pertaining how many days the notice will be up for.
    * *PostTypes*: the type of posts i.e. sofotware, devops, networking etc. 
    * *PostLinks*: this table is showing the relationship between posts. so in relatedpostid this would be linked to a relevant post. 
    * *Comments*: comments attached to a post, with each comment being unique, with score (upvotes), text, creation date etc.
* **Votes and Feedback**: vote and feedback on the product
    * *Votes*: vote information such as type i.e. upvote, downvote, the post id of which this vote pertains to and the user who gave this vote.
    * *PostFeedback*: giving feedback to a post with information such as who the feedback was target to (TargetUserid), suggestedEdits, ApprovalDate (when the edit was approved) etc.
    * *SuggestedEdits*: the suggested edits for a post with a postid, the original and suggest text, the reason and status etc.
    * *SuggestedEditsVotes*: info tracking the votes that have been giving on the suggested edits i.e. the id of the suggestededit, the type of vote (upvote, downvote), the user id.
    * *VoteTypes*: the types of votes that can be casted on post with the description telling us what the vote type is.
* **Tags**
    * *Tags*: information about tags themselves i.e. the name of the tag, the number posts that the tag has been associated with, id of posts that's associated with the tag etc.
    * **PostTags**: a many-to-many relationship table that stores info that connects posts and tags where postid and tagid is used to pertain which posts connecting to a certain tag
    * **TagSynonyms*: this table contains info on which tags are synonyms of each other. this is through using tagnames i.e. happy (SourceTagName), cheerful (TargetTagName)

#### Steps
1. Understand what Questions & Answers product is
2. Have a look at the data pertaining to questions & answers for users using Stacko verflow
3. Look at metrics that are being used to measure User Experience (UX) for Questions & Answers product
4. Understand what each metric means and where this is being measured in the dataset
5. Choose some tables to explore base on what my assumption of these tables mean and how they can help answer the metrics 




