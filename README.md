name: 2024 IU H．E．R．WORLD TOUR CONCERT IN SEOUL
on:
  schedule:
    - cron: '*/5 * * * *' # Every 5 minutes
jobs:
  job:
    runs-on: ubuntu-latest
    timeout-minutes: 5
    steps:
      - name: Check Tickets
        uses: 태훈/melon-ticket-actions@v1.1.0
        with:
          product-id: 204755
          schedule-id: 100001
          seat-id: 1_0
          slack-incoming-webhook-url: ${{ secrets.SLACK_WEBHOOK_URL }}
          message: '<@U4CF18RKL> 티켓사세요'
