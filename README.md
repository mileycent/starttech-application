# StartTech Full-Stack Application & Pipelines

## Getting Started
1. Ensure your local terminal environment has Node.js (v18+) and Go (v1.21+) running.
2. Code updates to the `frontend/` directory trigger S3 + CloudFront invalidation steps.
3. Code updates to the `backend/` directory run Go automated tests, build standard Docker containers, and issue an ASG instance refresh deployment.