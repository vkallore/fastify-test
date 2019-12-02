# Fastify Try

## Run Server

```
npm i
npm run dev
```

### Errors

#### `ENOSPC`

```
[nodemon] Internal watch failed: ENOSPC: System limit for number of file watchers reached, watch 'PATH_TO_ROOT'
```

If you come across above error, run the below command
```
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```