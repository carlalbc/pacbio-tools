# 🧬 pacbio-tools

Helper scripts and notes for processing PacBio Onso data at the Institute of Medical Genetics, UZH.

---

## 📂 What’s Included

- [`obc2fastq_quickstart_guide.md`](./obc2fastq_quickstart_guide.md): Step-by-step guide for running `obc2fastq`
- [`SampleSheet_template.csv`](./SampleSheet_template.csv): Example `SampleSheet.csv` for demultiplexing
- [`obc2fastq_command_template.txt`](./obc2fastq_command_template.txt): Ready-to-use command-line example
- [`obc2fastq_error_cheatsheet.txt`](./obc2fastq_error_cheatsheet.txt): Common errors and how to troubleshoot them

---

## 🚀 Quick Start

1. **Log in** to the PacBio server as user `smrt`  
2. **Prepare** your `SampleSheet.csv` (example included)
3. **Run** `obc2fastq` using the command line template

See full instructions in the [Quickstart Guide](./obc2fastq_quickstart_guide.md)

---

## 🛠️ Requirements

- Access to the PacBio analysis server
- `obc2fastq` installed system-wide
- 8bp barcodes required for demultiplexing

---

## 💡 Notes

- For login credentials, please contact **Beat** — per institute policy, credentials are not shared via email.
- You can use the error cheatsheet to help diagnose common issues when running `obc2fastq`.

---

## 👤 Maintainer

Created and maintained by **Carla Bello**  
Feel free to open issues or contribute if this repo expands in the future.
