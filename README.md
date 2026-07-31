>[!WARNING]
>CURRENTLY UNDER DEVELOPMENT



# Secure Enterprise CSV Data Management and Auditing System

A full-stack web application featuring user authentication, role-based access control, and dynamic in-memory CSV parsing. Built to allow authenticated users to upload tabular data, map columns dynamically, and securely filter custom data views.

1. Role-Based Access Control (RBAC) Middleware
Protect your API routes so that only authorized users can perform specific actions.
Standard User: Can upload a CSV, select headers to view, and download their filtered results.

Operator: Can execute batch transformations, handle queued files, and monitor processing speeds.

Admin: Has full control to manage user roles, delete accounts, and inspect system-wide audit logs.

---

## How it works

```
git clone https://github.com/gutiluis/Get-users-passwords-from-csv.git
cd
python3 main.py
```

---

## Features

- Secure Authentication: Implements hashed passwords (using bcrypt), role-based access, and secure token-based authentication (JWT or HTTP-only cookies).

- Dynamic Column Mapping: Instead of hardcoding which columns to fetch, backend dynamically reads the CSV header row (df.columns.tolist()) and send those options back to the frontend so the user can select columns via a multi-select dropdown.

- Audit Logging: Stores metadata in database every time a file is processed (e.g., timestamp, file name, rows processed, requested columns) to show a history of user activity without saving the actual sensitive payload.

- Privacy & Data Hygiene: Implements an automated cleanup mechanism or strict in-memory processing so upload files never permanently saved to the server's disk.

---

## Tech-Stack:

- React
- Next.js
- Python (FastAPI)
- SQLAlchemy
- PostgreSQL
- JavaScript

---

## Contributing

If you are interested in reporting/fixing issues and contributing directly to the code base, please see [CONTRIBUTING.md](https://github.com/gutiluis/.github/blob/main/CONTRIBUTING.md) for more information on what we're looking for and how to get started.

---

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](https://github.com/gutiluis/.github/blob/main/CODE_OF_CONDUCT.md).

---

## Security Policy

If you discover a security vulnerability, please review our [Security Policy](https://github.com/gutiluis/.github/blob/main/SECURITY.md) for reporting guidelines.

---

## Support

If you run into any issues or have questions, please check our [SUPPORT.md](https://github.com/gutiluis/.github/blob/main/SUPPORT.md) file for guidance, or reach out through one of our community channels below.

---

## Community

Info on reporting bugs, getting help, finding third-party tools and sample apps, and more can be found on our **Community** channels:
* **Discord:** [Community channel](https://discord.gg/5xdAFuadP)
* **Slack Workspace:** [technobool.slack.com](https://technobool.slack.com)
* **GitHub Discussions:** [Open a discussion](https://github.com/gutiluis/[reponame]/discussions)

---

## License

[MIT LICENSE](LICENSE)
