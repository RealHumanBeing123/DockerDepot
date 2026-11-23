# DockerDepot

Like cURL Craft, but for Docker, and still offline. The HTML file is all that you need.

Pick a command, choose your options, and get a ready-to-run `docker` command that updates as you go. Nothing is sent anywhere: the page makes no network requests.

Commands covered:
- Running containers: run (name, ports, volumes and mounts, environment variables, restart policy, network, memory and CPU limits, GPUs, capabilities, health check), exec, ps, logs, stop, start, restart, kill, pause and rm.
- Building: build (tags, Dockerfile, build arguments, target stage, no cache, platforms, push or load, secrets), tag, pull and push.
- Compose: up, down, start, stop, restart, ps, logs, build, pull, exec, run, config and images, with files, project name, profiles, scaling and volume removal.
- Looking around: inspect (with a field picker), stats, images and system (disk usage, info, events).
- Infrastructure: network and volume management.
- Housekeeping: prune (containers, images, volumes, networks, build cache or everything), login and cp (copy files in and out of a container).

Beyond the options themselves, I added a few more things:

- Explanation panel: it breaks the command into parts and says what each one does.

- Quick-start recipes: 16 examples such as a web server, a throwaway shell, a database with a saved volume, serving a local folder, a fresh rebuild, starting and stopping Compose, following logs and freeing disk space.

- Shell and syntax choices: bash/zsh, PowerShell or cmd, with the right quoting, and short or long flags.

- Warnings: for ports open to your whole network, unpinned `latest` images, privileged mode, mounting the Docker socket, deleting volumes, a detached container that vanishes with its logs (`--rm`), `--rm` combined with a restart policy (Docker refuses that), and logging in with a password (it suggests piping the password in so it stays out of your shell history).

Only the options for the command you pick are shown, so the page stays short.

Less common options (Swarm, buildx bake, contexts, plugins, advanced logging drivers) are left out. See `docker --help` for those.

Just open `DockerDepot.html` in any browser. It works with no internet connection.
