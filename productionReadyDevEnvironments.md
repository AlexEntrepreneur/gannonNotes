# Production-Ready Dev Environments

### Notes by Gannon Darcy

- Note: just make 2 staging environments off the rip.

- The staging environment EXACTLY equals production. if your production environment uses netlify, then staging needs it too. Any variables, caps, 3rd party API's, literally anything.... thats in production, needs to be mirrored in staging BUT needs to be SEPARATE from production. (so if you use SendGrig in production, you'll make a separate SendGrid account/instance for production and staging, yet set them up equally for those two instances). The goal is for them to mirrors... but parallel. Staging can never touch production (and thus cannot break production, although production CAN update staging such as updating/syncing your staging DB with current Production DB)

- You can send the staging server to the external stakeholder to get their feedback before those things are seen on production.

- Certain things you can ONLY test on servers (that you can't test on your local machine) like CORS issues, issue with hosting (heroku issues), parts of 3rd party APIs, some native functionality of mobile devices (cameras, location, gyroscope, etc)

# Flow/Timeline:

## **Dev**

- make a feature-named branch if it doesn't already exist.
- making init commit
- make a draft PR
- more commits
- code review
- deploy this INDIVIDUAL branch to staging.

## **Staging**

- Deploy to relevant staging server (netlify or heroku, both if the PR affects both)
- (if there is a lot of "stepping on toes" with the one set staging server(s) then make a second set of staging servers to avoid this and work on communication)
- Ask someone else on the team to QA the newly deployed staging server, AFTER you check what you've just deployed first.
- Stakeholder Review (a very probable bottleneck, thus a good reason for the secondary and tertiary staging servers)
- Keep pulling master and merging into this branch to make sure it's all up-to-date before final merge to avoid any surprises.
- Merge to master

## **Production**

- The newly merged branch should be deployed to production now.
- Double check to make sure that production doesn't magically break (doing this should avoid that from ever happening.... but sometimes weird things happen).
- If production EVER breaks (even if it's 2am) rally the team and fix it ASAP (if you have real people using the application.

## **Misc**

- CI (continuous integration) for production only, not staging. Staging needs to be click-to-deploy. Checkout CircleCI
- Uptime (you want to monitor production with several alerts to let you/the team know if production goes down. Its good to have it for staging too but it's mission-critical for production).
- For URL's make it:
  - staging.myapp.com
  - staging2.myapp.com
  ***
  Production will be:
  - Myapp.com
  - Make a team Email account and sign up for the accounts (netlify, heroku, API's, etc) with that team account and share the email/login credentials with your team members.
  - Pick a team member to go through this with you, it's a great learning opportunity to pair program.
