## Writing Good Bug Reports and Feature Requests

File a single issue per problem and feature request. Do not include multiple bugs or feature requests in the same issue.
The more information you can provide, the more likely someone will be successful reproducing the issue and finding a fix. 
Take advantage of Github Markdown styling to make your issue easier to read. For example, Wrap single line code statements or logs in single backticks: \` code here \`. Wrap multi-line in triple backticks: \``` multi-line code here \```. 

#### Please include the following with each issue:

* Reproducible steps (1... 2... 3...) and what you expected versus what you actually saw.
* Log output from Ansible or other relevant services, ideally linking to a Gist for longer log output.
* Operating System of server 
* Operating System of client
* Version of Ansible using output from `ansible --version` 

Don't feel bad if we can't reproduce the issue and ask for more information!

## Contributing Fixes
If you are interested in fixing issues and contributing directly to the code base, please feel free to submit a PR.
