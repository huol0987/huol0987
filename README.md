name: Melon Ticket
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
          slack-incoming-webhook-url: ${{ https://discord.com/api/webhooks/1213416414187098182/LkaGPE7TlKmSy0lujodM4FCZS8KUt1mLQ0OmNjXG1YSdwJSV_79lsCLChAUI4lDPQs2t }}
          message: '<@U4CF18RKL> 티켓사세요'
