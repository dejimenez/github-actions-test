secrets to see debug messages


variables
GITHUB_SHA the commit id of the last commit
GITHUB_REPOSITORY name of the repository
GITHUB_WORKSPACE the directory where we are located, similar to pwd

for crom checking
https://crontab.guru/

for starting the workflow with the event "repository_dispatch"
it is possible to start an event from request_dispatch that is trigger using a http request to:
https://api.github.com/repos/user/github-actions-test/dispatches
headers needs to be changed(Accept and Content/Type)
body needs to be send with event_type:
{
    event_type: "build",
    client_payload: {
        key: value
    }
}

when we send client_payload it could be accessed by using github objet in the workflow yml