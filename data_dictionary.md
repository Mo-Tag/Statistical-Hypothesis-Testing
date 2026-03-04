# TikTok Dataset – Data Dictionary

| Column Name                  | Data Type   | Description |
|------------------------------|-------------|-----------|
| `claim_status`               | object      | Whether the video is a **claim** (potentially misleading) or **opinion** (personal viewpoint) |
| `video_id`                   | int64       | Unique identifier for each video |
| `video_duration_sec`         | int64       | Length of the video in seconds (range: 5–60) |
| `video_transcription_text`   | object      | Auto-generated transcription of the spoken audio |
| `verified_status`            | object      | Account verification status: **verified** or **not verified** (key variable for this hypothesis test) |
| `author_ban_status`          | object      | Author's current status: **active**, **under review**, or **banned** |
| `video_view_count`           | float64     | Total number of views the video received (**primary metric** for t-test) |
| `video_like_count`           | float64     | Total number of likes |
| `video_share_count`          | float64     | Total number of shares |
| `video_download_count`       | float64     | Total number of downloads |
| `video_comment_count`        | float64     | Total number of comments |

**Notes:**
- 298 rows contained missing values in engagement columns and were dropped for the hypothesis test.
- `verified_status` and `video_view_count` were the focus of the two-sample t-test.
- Engagement metrics are heavily right-skewed (typical for social media data).
