# S3-Bucket-Analysis-Optimization
# S3 Bucket Analysis and Optimization

This repository contains a Python script to analyze and optimize S3 bucket metadata. The goal is to:
- Print a summary of each S3 bucket (Name, Region, Size, and Versioning status).
- Identify and provide recommendations for buckets that are large (size > 50 GB), unused, or inactive.
- Generate cost reports for S3 buckets, grouped by region and department.
- Highlight buckets with high storage usage (> 50 GB), suggest cleanup operations, and move large inactive buckets to Glacier for cost savings.
- Provide a final list of buckets to delete and archival candidates to Glacier.

## Requirements

- Python 3.12.3
- AWS CLI (Optional, for cleanup and archival)


1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/S3-Bucket-Analysis-Optimization.git

2. Place your buckets.json in the same directory as the script or update the script to reference the correct path.


How to Run the Script:

1]Navigate to the project folder:
  cd DevSRE

2]Place your buckets.json in the same directory.

3]Run the script:
python3 s3_bucket_analyzer.py


Files:
1]s3_bucket_analyzer.py: Python script for analyzing S3 bucket data.
2]buckets.json: Sample JSON file with metadata for S3 buckets.


Challenges Faced
Accessing S3 Metadata: The hardest part of the project was understanding how to properly access and analyze metadata such as bucket size, region, and access history.
Handling Large Buckets: Moving large data to Glacier requires understanding AWS S3 storage classes, which was a new concept for efficient data management.


