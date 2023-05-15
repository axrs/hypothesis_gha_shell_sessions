# Hypothesis: GitHub Actions Shell Cascade

I believe shell contexts within GitHub Actions steps are independent isolated from the previous steps.

## Result:

GitHub Actions steps indeed do NOT cascade set variables between steps or step/runs.

It is worth nothing however that the default bash shell runs with the internal command `bash --noprofile --norc -eo pipefail {0}`.

https://docs.github.com/en/enterprise-cloud@latest/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idstepsshell
