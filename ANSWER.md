## Part A: Promo Image Inspection

1. **Exposed Ports:**
   - **Answer:** 3000/tcp, 80/tcp
   - **Command Used:** `docker image inspect kamthornsa/ksu-promo:1.0 --format='{{json .Config.ExposedPorts}}'`

2. **Container Startup Command:**
   - **Answer:** Entrypoint: ["/docker-entrypoint.sh"] | Cmd: ["nginx","-g","daemon off;"]
   - **Command Used:** `docker image inspect kamthornsa/ksu-promo:1.0 --format='Cmd: {{json .Config.Cmd}} | Entrypoint: {{json .Config.Entrypoint}}'`

3. **Base Image:**
   - **Answer:** Alpine Linux v3.24
   - **Command Used:** `docker run --rm kamthornsa/ksu-promo:1.0 cat /etc/os-release`