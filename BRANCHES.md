# How To Name Your Branches - The Method I Use...

![fTa5D](https://user-images.githubusercontent.com/14003326/217037812-70233528-4632-4b41-9209-7354944b3c99.png)


A branching strategy is a convention or a set of rules that specify when branches get created. It helps teams and developers by describing the naming guidelines of branches and elaborates on what use the branches should have, and so on. With a lack of appropriate naming conventions, the code maintenance team suffers numerous confusions and complications. Git branching naming convention supports the organic growth of a codebase in a systematic way. It helps in separating the work strategically. Here we will go over the two main categories of Git branches and we will go over them below.

## The Two Categories of Git branches

- Regular Branches
  - ["main"](#main)
  - ["dev"](#development-dev)
  - ["test"](#qa-or-test-branch)

- Temporary Branches
  - ["fix"](#fix)
  - ["wip"](#wip)
  - ["bug"](#bug)
  - ["feat"](#feat)

## Regular Branches

Regular branches are branches that are available permanently in the repository, the naming convention of regular branches is easy and straightforward. They are usually named `main` when you initialize the repository. If you are going to be making a large project it is a good idea to go ahead and name the other branches for the purposes of development. These are usually named `main`, `dev`, (`test` or `qa`), `fix`, and `feat`. We will go over each of these below and explain their uses.

### Main

The `main` branch is the default branch available in the Git repository. Team members need to keep the `main` branch stable and updated. It usually is stable and doesn't allow direct check-in. Merging is possible only after code review.

### Development (`dev`)

`dev`, this is the main development branch, it restricts developers from adding any changes in the master branch directly. Before merging to the master, changes made in the dev branch undergo reviews and tests. Some large companies will require developers to add their name to the branch so they are easily tracked such as `yosileyid-dev-audio.plugin`

### QA or test branch

This branch holds the `qa` or `test` codes and automation testing of the implemented changes. It ensures a stable codebase for the production environment through the testing process.

## Temporary Git branches

Team members can create and delete these branches whenever it is required. They are not meant to stay in production. If they address the "Issue" then push them upstream to `test` and delete the branch. Below are the most common names used for temp branches. There are a large number of recommended conventions and formats, following which could be a challenging task. The best practices of the Git branch naming convention are up to you and your company as to how to best use these. The methods I have used before as detailed below. One of the best methods to improve efficiency is by adding a word that categorizes the branch. 

The general idea is to use short words. The word selection could be anything that suits your working system. With the help of the category word, it is effortless to identify the purpose of the Git branch and attend to it. Prefixes such as; hotfix, feature, chore, or any other variant to categorize a task, increase the work requiring more decision-making while naming. With unique issue tracker IDs, you are essentially marking the task's category in the tracker and adding many useful contexts.

### WIP
`wip-{feature.name}`: Work in progress and needs your attention. Developers mostly work on several issues at a given time, and an issue tracker helps to connect the working branch with relevant tasks. It makes tracking team progress very easy.

### FIX
`fix-#{bug.number}`: This usually fixes something that broke and doesnt require an entire rewrite of the code base.

### BUG
`bug-#{bug.number}`: A bug or an error that needs fixing promptly. Using an external issue tracking ID in the branch name can facilitate tracking the progress from external systems.

### FEAT
`feat-name`: A new feature to be implemented. This is usually something to merge into `test` as it is added. It will be buggy and require testing from various devices and users before it can be pushed into production.

### Using hyphen or slash separators

The preference between a hyphen, slash, or underscore separator is based on you and your team's choice. The idea is to keep it tightly consistent. Without the separators, the names become more challenging to read, creating confusion for the team. Using separators such as underscores, you can improve the readability and make the name more comfortable to manage. Separators are especially more significant if you are dealing with a vast number of branches. Many companies use the technique of adding the author's name to the branch names such as  (`yosileyid-#11457-bug` || `yosileyid_#11457_bug`), (`yosileyid-#5562-feat` || `yosileyid_#5562_feat`) and so on. This method helps to track the work of different developers. With further requirements, progressive additions are also possible. Using only numbers in the branch name's issue ID can lead to more confusion for the team. Such confusion during the merging process of Git branches may lead to a lot of mistakes.