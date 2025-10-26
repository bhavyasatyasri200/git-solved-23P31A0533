# My Git Mastery Challenge Journey

## Student Information

* Name: Bhavya Saty Sri
* Student ID: 23P31A0533
* Repository: [https://github.com/bhavyasatyasri200/git-solved-23P31A0533](https://github.com/bhavyasatyasri200/    git-solved-23P31A0533)
* Date Started: 26-10-2025
* Date Completed: 26-10-2025

## Task Summary

Cloned the instructor's repository with pre-built conflicts and resolved all merge conflicts across multiple branches using proper Git workflows. This included handling complex conflicts, testing the resolved code, and documenting the process.

## Commands Used

| Command         | Times Used | Purpose                                    |
| --------------- | ---------- | ------------------------------------------ |
| git clone       | 1          | Clone instructor's repository              |
| git checkout    | 20+        | Switch between branches                    |
| git branch      | 10+        | View and manage branches                   |
| git merge       | 2          | Merge dev and conflict-simulator into main |
| git add         | 30+        | Stage resolved conflicts                   |
| git commit      | 15+        | Commit resolved changes                    |
| git push        | 10+        | Push to repository                         |
| git fetch       | 2          | Fetch updates from instructor              |
| git pull        | 1          | Pull updates                               |
| git stash       | 2          | Save temporary work                        |
| git cherry-pick | 1          | Copy specific commit                       |
| git rebase      | 1          | Rebase feature branch                      |
| git reset       | 3          | Undo commits (soft/mixed/hard)             |
| git revert      | 1          | Safe undo                                  |
| git tag         | 2          | Create release tags                        |
| git status      | 50+        | Check repository state                     |
| git log         | 30+        | View commit history                        |
| git diff        | 20+        | Compare changes                            |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml

* Issue: Production used port 8080, development used 3000
* Resolution: Created unified config with environment-based settings
* Strategy: Keep production as default, add dev as optional
* Difficulty: Medium
* Time: 15 min

#### Conflict 2: config/database-config.json

* Issue: Different database hosts and SSL modes
* Resolution: Created separate profiles for production and development
* Strategy: Restructured JSON to support both environments
* Difficulty: Medium
* Time: 10 min

#### Conflict 3: scripts/deploy.sh

* Issue: Different deployment strategies (production vs docker-compose)
* Resolution: Added conditional logic based on DEPLOY_ENV variable
* Strategy: Script handles both environments dynamically
* Difficulty: Hard
* Time: 20 min

#### Conflict 4: scripts/monitor.js

* Issue: Different monitoring intervals and log formats
* Resolution: Environment-based configuration object
* Strategy: Used process.env.NODE_ENV to determine behavior
* Difficulty: Medium
* Time: 15 min

#### Conflict 5: docs/architecture.md

* Issue: Different architectural descriptions
* Resolution: Merged both descriptions into a comprehensive document
* Strategy: Created sections for each environment
* Difficulty: Easy
* Time: 10 min

#### Conflict 6: README.md

* Issue: Different feature lists and version numbers
* Resolution: Combined all features with clear environment labels
* Strategy: Organized features by category
* Difficulty: Easy
* Time: 10 min

### Merge 2: main + conflict-simulator (6 files)

#### Conflict 1: config/app-config.yaml

* Issue: Experimental version added multi-port and AI settings
* Resolution: Preserved production as primary, added experimental config section
* Strategy: Environment-specific sections for production, development, experimental
* Difficulty: Medium
* Time: 15 min

#### Conflict 2: config/database-config.json

* Issue: Experimental version introduced distributed cluster, AI optimization, and multi-region replication
* Resolution: Added experimental block, kept production and development separate
* Strategy: Clear separation of environments
* Difficulty: Hard
* Time: 20 min

#### Conflict 3: scripts/deploy.sh

* Issue: Experimental deployment script had AI and multi-cloud logic
* Resolution: Production deployment unchanged, added experimental block as optional
* Strategy: Conditional deployment based on DEPLOY_ENV
* Difficulty: Hard
* Time: 25 min

#### Conflict 4: scripts/monitor.js

* Issue: Experimental monitoring used AI predictions, multi-cloud metrics
* Resolution: Kept production/dev monitoring intact, experimental features optional
* Strategy: Environment-based configuration object
* Difficulty: Hard
* Time: 20 min

#### Conflict 5: docs/architecture.md

* Issue: Experimental architecture described event-driven, AI-enhanced system
* Resolution: Added experimental section while preserving production/dev architecture
* Strategy: Separate sections for each environment
* Difficulty: Medium
* Time: 15 min

#### Conflict 6: README.md

* Issue: Experimental README added AI features and advanced quick-start instructions
* Resolution: Kept production as default, added experimental info as optional section
* Strategy: Clear labeling of features by environment
* Difficulty: Medium
* Time: 15 min

## Most Challenging Parts

1. Understanding Conflict Markers: Initially confused by <<<<<<<, =======, >>>>>>> symbols. Learned HEAD is current branch and the other side is incoming changes.
2. Deciding What to Keep: Choosing between conflicting code required careful review of both sides.
3. Complex Logic Conflicts: deploy.sh had completely different logic; had to combine approaches.
4. Testing After Resolution: Ensuring resolved code worked correctly in all environments was crucial.

## Key Learnings

### Technical Skills

* Mastered conflict resolution across multiple environments
* Deep understanding of merge conflict markers
* Learned to use git diff and git log effectively
* Practiced advanced Git commands: rebase, cherry-pick, reset, revert
* Maintained separate environment configurations (production, development, experimental)

### Best Practices

* Read both sides before resolving conflicts
* Test code before committing
* Write detailed merge commit messages
* Commit atomically and document changes clearly
* Maintain a clean branch strategy

### Git Workflow Insights

* Conflicts are normal, not errors
* Take time to understand both changes
* Use environment-specific configurations
* When in doubt, ask for clarification
* Keep calm and read carefully
* Backup work with git stash before pulling

## Reflection

This challenge taught me that merge conflicts aren't scary—they are Git asking "which version do you want?". Understanding each side’s intention is key.

Hands-on practice with all Git commands (especially rebase and cherry-pick) gave me confidence to handle conflicts in real projects. I now understand the difference between merge and rebase, and when to use each. Most importantly, git reflog is a lifesaver!
