# sit737-2025-prac5p
# SIT737-2025-Prac5P

## Setup and Deployment

### 1. Clone the Repository
```sh
git clone https://github.com/KT-277/sit737-2025-prac5p.git
cd sit737-2025-prac5p
```

### 2. Build and Start Containers
```sh
docker-compose up --build -d
```

### 3. Check Running Containers
```sh
docker ps
```
Ensure all containers are running and healthy.

### 4. Inspect Container Health (Optional)
```sh
docker inspect --format="{{json .State.Health}}" <container_id>
```
Replace `<container_id>` with the actual container ID from `docker ps`.

### 5. Push Changes to Repository
```sh
git add .
git commit -m "Updated repository"
git pull origin main --rebase
git push -u origin main
```
If `git push` is rejected due to remote changes, resolve conflicts and push again.

### 6. Stop and Remove Containers (If Needed)
```sh
docker-compose down
```

## Notes
- Ensure Docker and Git are installed and running before executing these commands.
- If `git push` is rejected, use `git pull origin main --rebase` before retrying.
- Ports `3000` and `8080` are mapped correctly as per `docker ps` output.
