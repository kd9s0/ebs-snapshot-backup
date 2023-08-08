# EBS Snapshot Backup

This repository contains a script to create EBS snapshots for point-in-time backups.

## Requirements

- AWS CLI installed and configured with appropriate IAM credentials.
- Replace `your_ebs_volume_id_here` in `create_snapshot.sh` with your actual EBS volume ID.

## Features

- Creates an EBS snapshot with a timestamp-based description.
- Retains only the latest N snapshots (controlled by `num_snapshots_to_retain` in the script).
- Logs events to a file (`snapshot_log.txt`).

## Usage

1. Clone the repository:

```bash
git clone https://github.com/kd9s0/ebs-snapshot-backup.git
cd ebs-snapshot-backup
```

2. Make create_snapshot.sh executable:
```
chmod +x create_snapshot.sh
```

3. Run the script to create an EBS snapshot:
```
./create_snapshot.sh
```