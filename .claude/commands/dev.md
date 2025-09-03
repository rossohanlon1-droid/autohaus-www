# Development Commands

Start the Jekyll development server using Docker.

## Usage

```bash
docker compose up
```

This command will:
- Start Jekyll server on `http://localhost:4000`
- Enable live reload on port 35729
- Mount the project directory for real-time changes
- Use Docker volumes for gem caching

## Options

- `docker compose up -d` - Run in detached mode (background)
- `docker compose up --build` - Rebuild container (after Gemfile changes)
- `docker compose logs -f` - View logs
- `docker compose down` - Stop and remove containers