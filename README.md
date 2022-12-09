# GitHub-Action-external-webhook-trigger

[![badge](https://github.com/ben1one/GitHub-Action-external-webhook-trigger/actions/workflows/webhook.yml/badge.svg)](https://github.com/ben1one/GitHub-Action-external-webhook-trigger/actions/workflows/webhook.yml)

## Personal access tokens
https://github.com/settings/tokens

## Create a repository dispatch event
https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#create-a-repository-dispatch-event

## Sample request
Note: The domain is `api.github.com` not `github.com`
```
curl --location --request POST 'https://api.github.com/repos/{owner}/{repo}/dispatches' \
--header 'Accept: application/vnd.github+json' \
--header 'Authorization: Bearer <YOUR-TOKEN>' \
--header 'X-GitHub-Api-Version: 2022-11-28' \
--header 'Content-Type: application/json' \
--data-raw '{"event_type": "webhook"}'
```
