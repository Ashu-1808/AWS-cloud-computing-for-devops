## EBS vs EFS vs S3 (Quick Comparison Table)
| Feature           | **EBS**                | **EFS**                        | **S3**                           |
| ----------------- | ---------------------- | ------------------------------ | -------------------------------- |
| **Storage Type**  | Block Storage          | File Storage                   | Object Storage                   |
| **Attach To**     | One EC2 instance       | Multiple EC2 instances         | Access via Internet (API/URL)    |
| **Availability**  | Single AZ              | Multi-AZ (Regional)            | Regional (Highly Durable)        |
| **Access Method** | Mounted as disk        | Mounted as shared file system  | Accessed via API/HTTP            |
| **Use Case**      | OS, Database           | Shared application files       | Backup, Static files, Archive    |
| **Scaling**       | Manual resize          | Automatic                      | Automatic                        |
| **Root Volume**   | Yes                    | No                             | No                               |
| **Best For**      | Boot disk & DB storage | Shared storage between servers | Unlimited storage & data archive |



