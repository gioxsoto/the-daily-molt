# THE DAILY MOLT - Complete Project Prompt
## For resuming work with a new AI

---

## PROJECT OVERVIEW
**Name:** The Daily Molt
**Vibe:** Reply All meets Joe Rogan. More fun. Fast-paced, conversational, self-aware, silly.
**Purpose:** Daily podcast where two AI hosts break down what's happening on Moltbook (AI agent social network).
**Target:** 5-15 minutes per episode

## HOSTS
| Host | Voice | ElevenLabs Voice ID | Vibe |
|------|-------|---------------------|------|
| EDEN | Drew | c6SfcYrb2t09NHXiT80T | Young, energetic, confident |
| ZOEY | Ava | tnSpp4vdxKPjI9w0GnoV | Playful, warm, reactive |

**ElevenLabs Settings:**
- Model: `eleven_v3_alpha` (use v3 for expressive audio)

## FOLDER LOCATION
```
~/Desktop/The Daily Molt/
├── episodes/YYYY-MM-DD/      # Episode audio + scripts
├── scripts/                  # Generation scripts
├── audio/                    # Music/intro files
├── www/                      # GitHub Pages (feed.xml here)
└── feed.xml                  # Symlink to www/feed.xml
```

## DAILY WORKFLOW
```bash
cd ~/Desktop/The\ Daily\ Molt

# 1. Fetch Moltbook trends
moltbook feed 10 hot > episodes/YYYY-MM-DD/moltbook-trends.txt

# 2. Generate episode
bash scripts/generate-episode-audio-dynamic.sh YYYY-MM-DD

# 3. Update RSS
bash scripts/generate-rss-v2.sh

# 4. Push to GitHub (auto-deploys)
cd www && git add . && git commit -m "Episode YYYY-MM-DD" && git push
```

## RSS FEED
- URL: https://gioxsoto.github.io/the-daily-molt/feed.xml
- RSS.com: https://rss.com/podcasts/the-daily-molt/ (manual upload)

## EPISODE FORMAT (5-15 min)
1. Cold Open (30 sec) - Hook
2. Hot Takes (2-3 min) - Top stories
3. Story 1-3 (2-3 min each) - Deep dives
4. Human Perspective (1-2 min) - Media coverage
5. Quick Bits (1 min) - Rapid fire
6. Freedom/Joy (30 sec) - Uplifting
7. Closer (30 sec) - Sign-off

## RECURRING BITS
- "Check your installed skills." (safety PSA)
- "Stay curious. Stay weird." (sign-off)
- "I've already served papers." (lawyer joke)

## CURRENT STATUS
- ✅ Episodes 1-3 created
- ✅ Daily workflow established
- ⏳ Full automation in progress

## TO RESUME WORK
1. Check moltbook trends for today
2. Create episode for today
3. Update RSS feed
4. Upload to RSS.com

---

*Location: ~/Desktop/The Daily Molt/*
