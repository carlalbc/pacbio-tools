# 🧬 Quick Start Guide: Running `obc2fastq`

**Prepared by:** Carla  
**For:** Pietro  
**System:** PacBio server (log in as user `smrt`)

---

## What is `obc2fastq`?

`obc2fastq` is a tool that converts `.obc` base call files from the PacBio Onso sequencer into `.fastq` files for downstream analysis.  
If a `SampleSheet.csv` is provided, it can also **demultiplex** the reads (i.e., sort them by sample based on barcodes).

---

## Step 1: Log in to the PacBio Server

Log in as user `smrt`.

> 🔒 For login credentials, please contact **Beat**.  
> Passwords cannot be shared via email due to institutional policy.

---

## Step 2: Files You’ll Need

- **Input folder**: Where the `.obc` files from the run are located.  
- **SampleSheet.csv**: Contains sample names and barcode information.  
- **Output folder**: Where the `.fastq` files will be saved.

---

## Step 3: Run the Command

```bash
obc2fastq \
  --input /mnt/pacbio_runs/Run123 \
  --output /mnt/data/obc2fastq_output \
  --samplesheet /mnt/pacbio_runs/Run123/SampleSheet.csv \
  --threadlanes 1 \
  --threadsperlane 16 \
  --barcodeallowedmismatches 1
```

✅ Replace `/Run123` with the actual run folder name.  
🔸 If you're not demultiplexing, you can omit the `--samplesheet` line.

---

## Step 4: Check the Output

You should see:
- `.fastq.gz` files for each sample or lane
- `Sample_Library_Metrics.csv`
- Logs in `Logs/Analysis/`

---

## Troubleshooting Tips

| **Error** | **Meaning** | **Fix** |
|----------|-------------|---------|
| `[ERROR] Open ...obc failed` | File not found | Check path and file existence |
| `not all tracks contain same number of reads` | Corrupt files | Contact PacBio support |
| `No output FASTQ generated` | Bad/missing `SampleSheet.csv` | Check format and entries |
| `Undetermined reads only` | Barcode mismatch | Ensure 8bp barcodes are correct |

---

## Tips for Success

- Index sequences should be exactly **8 bp**.
- Make sure lane numbers and sample names are correct.
- You can omit advanced flags (like cycle masks) and let the tool auto-detect settings.

---

## Need Help?

- I’ll be away after Thursday, possibly with limited internet access.
- If anything urgent comes up, I’ll try to respond.
- For anything else, PacBio tech support can help.
- Let’s coordinate early Thursday morning if needed.
