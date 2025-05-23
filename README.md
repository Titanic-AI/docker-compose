# Temp Repo Navi
[Docker Compose](https://mygit.th-deg.de/schober-teaching/student-projects/ain-23-software-engineering/ss-25/7up/docker-compose)

[Model Backend](https://mygit.th-deg.de/schober-teaching/student-projects/ain-23-software-engineering/ss-25/7up/model-backend)

[Project Management](https://mygit.th-deg.de/schober-teaching/student-projects/ain-23-software-engineering/ss-25/7up/project-management)

[Web Backend](https://mygit.th-deg.de/schober-teaching/student-projects/ain-23-software-engineering/ss-25/7up/web-backend)

[Web Frontend](https://mygit.th-deg.de/schober-teaching/student-projects/ain-23-software-engineering/ss-25/7up/web-frontend)

# Requirements for Docker Compose
- The compose specification shall be managed in the docker-compose repository.
- All other required repositories are included in this repository via git submodules

# commands for submodule updates

```bash
cd docker-compose
git submodule update --remote --merge
git status
git add web-backend model-backend web-frontend
git commit -m "Update submodule pointers to latest commits"
git push origin jamal-dc
```

# running docker + caddy + Frontend

```bash
docker-compose build caddy
docker-compose up -d
website:  http://localhost:8080
```
# -----------------------------------------------------------------------------------------------

# docker + web-backend + swagger after running caddy
# swagger 

```bash
http://127.0.0.1:8000/docs
```
# access database
```bash
docker exec -it docker-compose-db-1 psql -U postgres -d Titanic_Databases
```
# check tables with 
```bash
\dt
```
# check users
```bash
SELECT * FROM "Registered_User";
```