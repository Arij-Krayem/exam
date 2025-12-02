# DevOps Test – Todo App (Arij Krayem)

## Steps Completed

1. Forked original repository
2. Cloned personal fork locally
3. Installed dependencies with npm
4. Tested application locally (npm run dev)
5. Fixed port 3000 conflict using netstat + taskkill
6. Wrote Dockerfile to run tests
7. Built Docker image (docker build)
8. Created docker-compose.yml
9. Tested Docker container
10. Created Jenkinsfile for CI pipeline
11. Configured Jenkins (SCM + Poll SCM)
12. Ran pipeline successfully

## Commands Used
git bash
git clone https://github.com/Arij-Krayem/exam.git
npm install
npm run dev
docker build -t exam-app .
docker compose up --build
