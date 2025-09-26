# Christine Bhoke Nchamah — Kuria Green & Gold Portfolio

This static website celebrates Christine ("Mama Arno") with a Kurian-inspired theme.  
Ready for GitLab Pages deployment.

## Deploy on GitLab Pages
1. Create a new GitLab project (e.g., `christine-portfolio`).
2. Push all files from this folder (index.html + assets).
3. Add `.gitlab-ci.yml` (example below).
4. Enable Pages in Settings.
5. Site will appear at `https://<namespace>.gitlab.io/<project>`.

## Minimal .gitlab-ci.yml
```yaml
image: alpine:latest
pages:
  stage: deploy
  script:
    - mkdir .public
    - cp -r * .public || true
    - mv .public public
  artifacts:
    paths:
      - public
  only:
    - main
```

---
Colors: Kuria Forest Green (#0F5132) & Gold (#F5B700)