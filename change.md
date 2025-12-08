Workflow: Modifying a Default LineageOS Repo

1. Fork on GitHub

  • Go to the LineageOS repository page.

  • Click Fork to your account.

2. Update Manifest (`.repo/local_manifests/veux.xml`)

  • Add `<remove-project name="LineageOS/original_repo_name" />`

  • Add `<project path="system/path" name="your_username/repo_name" remote="github" revision="lineage-23.0" />`

3. Sync Changes

```

repo sync --force-sync path/to/repo

```

4. Set Upstream & Branch

```

cd path/to/repo

git remote add upstream [suspicious link removed]

git checkout -b lineage-23.0

```

5. Modify & Save

  • Make your changes.

```

git add .

git commit -m "Your commit message"

git push -u github lineage-23.0

```

