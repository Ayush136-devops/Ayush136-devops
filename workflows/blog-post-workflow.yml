name: Latest blog post workflow

on:
  schedule:
    # Runs every hour
    - cron: '0 * * * *'
  workflow_dispatch: # Allows manual trigger from GitHub Actions tab

jobs:
  update-readme-with-blog:
    name: Update README with latest Medium posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://medium.com/feed/@ayushkhatal136"
          max_post_count: 5
          readme_path: README.md
          comment_tag_name: BLOG-POST-LIST
          gh_token: ${{ secrets.GITHUB_TOKEN }}
