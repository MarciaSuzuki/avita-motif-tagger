# AViTA Motif Tagger

Acoustic Motif Tagging Interface for the Tripod Method — Phase 2.3

## About

This app helps linguists tag discovered acoustic motifs with grammatical meanings. It's part of the Ready Vessels Project for AI-assisted Bible translation.

The motif data comes from Sateré-Mawé (Acts 12) processed through the acoustic pipeline.

## Folder Structure

```
avita-motif-tagger/
├── index.html              # Main application (self-contained)
├── README.md               # This file
└── motif_samples/          # Audio files (from Colab)
    ├── motif_000_bigram_0.wav
    ├── motif_000_bigram_1.wav
    └── ... (120 files total)
```

## Setup Instructions

### Step 1: Download the motif_samples folder

Go to your Google Drive: `satere_project/phase2_output/motif_samples/`

Download the entire folder (120 .wav files).

### Step 2: Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name it `avita-motif-tagger`
3. Set to **Public**
4. Click **Create repository**

### Step 3: Upload Files

**Option A: GitHub Web Interface**

1. Click **"uploading an existing file"**
2. Upload `index.html`
3. Create a folder called `motif_samples` and upload all 120 .wav files

**Option B: Git Command Line**

```bash
cd avita-motif-tagger
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/avita-motif-tagger.git
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **Deploy from a branch**
4. Choose **main** branch and **/ (root)**
5. Click **Save**

### Step 5: Access Your App

After 1-2 minutes, your app will be live at:

```
https://YOUR_USERNAME.github.io/avita-motif-tagger/
```

## How to Use

1. Click **Start Tagging**
2. Listen to the audio samples (click each to play)
3. Select a grammatical category (deixis, tense, aspect, etc.)
4. Select a subcategory for more detail
5. Add notes if needed
6. Click **Save & Next** to proceed
7. At the end, download the JSON export

## Categories

| Category | Description |
|----------|-------------|
| Deixis | Pointing words (this, that, here, there) |
| Tense | Time reference (past, present, future) |
| Aspect | Action shape (completed, ongoing, habitual) |
| Modality | Possibility, necessity, ability |
| Polarity | Affirmative, negative, question |
| Number | Singular, dual, plural |
| Person | 1st, 2nd, 3rd person |
| Case/Role | Agent, patient, benefactive, etc. |
| Other | Discourse markers, connectors |
| Unknown | Unclear or needs more examples |

## Export Format

The JSON export includes:

```json
{
  "export_type": "motif_tags",
  "export_date": "2026-01-17T...",
  "source": "AViTA Motif Tagger",
  "language": "Sateré-Mawé (Acts 12)",
  "total_motifs": 40,
  "tagged_count": 35,
  "motifs": [
    {
      "motif_id": "motif_000",
      "pattern": "U62_U33",
      "type": "bigram",
      "frequency": 146,
      "category": "deixis",
      "subcategory": "proximal (this/here)",
      "notes": "..."
    }
  ]
}
```

---

*Ready Vessels Project — University of the Nations / YWAM Kansas City*
