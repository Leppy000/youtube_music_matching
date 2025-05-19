# Project Purpose: Bridging Spotify Playlists with YouTube Music

## Overall Goal

The central aim of this project is to create a semi-automated workflow that allows a user to take their existing music playlists from Spotify and find corresponding tracks on YouTube Music. The process involves two main phases:

1.  **Exporting Spotify Playlist Data:** Extracting detailed track information (artist and song title) from all of a user's Spotify playlists into a structured, local format (an Excel spreadsheet).
2.  **Matching and Augmenting with YouTube Music Data:** Using the exported Spotify data to search for equivalent songs on YouTube Music, attempting to identify the best possible match, and then updating the local spreadsheet with the match status (e.g., "EXACT", "PARTIAL", "NOT FOUND") and a direct link to the YouTube Music track.

The ultimate purpose is to provide the user with an enriched dataset that maps their Spotify music library to YouTube Music, facilitating playlist recreation, music discovery, or simply creating a cross-platform reference of their music.

## Phase 1: Spotify Playlist Export to Excel

* **Purpose:** To create an organized, local, and machine-readable inventory of the user's Spotify playlists and the songs within them.
    * This serves as the foundational dataset for the subsequent matching phase.
    * It allows for offline review and backup of playlist contents.
    * The structured format (Excel) is chosen for its ease of use, readability, and compatibility with data manipulation libraries in Python (like Pandas).

## Phase 2: Matching Songs to YouTube Music & Updating Excel

* **Purpose:** To programmatically find the YouTube Music equivalents for songs identified in the Spotify export, and to record the success and details of these matches.
    * **Automate Playlist Recreation:** While not directly creating YouTube Music playlists in the current scope of the *matching strategy document*, finding the YouTube URLs is the first critical step towards enabling such functionality. The immediate goal is to identify the correct YouTube Music video ID.
    * **Assess Match Quality:** To provide a clear indication of how confident the script is in the match found (Exact, Partial, or Not Found). This helps the user understand where manual intervention or review might be needed.
    * **Create a Cross-Platform Reference:** The updated Excel file will serve as a bridge, linking specific Spotify tracks to their likely YouTube Music counterparts.
    * **Facilitate Manual Curation:** For tracks marked "NOT FOUND" or "PARTIAL", the user has a clear list of items requiring manual searching on YouTube Music, but with the initial legwork of data extraction already done.

## The Role of the Matching Strategy

The "Strategy for Matching Songs to YouTube Music" document specifically details the *methodology* for achieving the core task of Phase 2. Its purpose is to outline a robust, heuristic approach to:

* Intelligently search YouTube Music using data from the Excel file.
* Analyze and score potential matches based on various criteria (title similarity, artist presence, official audio keywords, etc.).
* Classify the best match found to provide actionable information to the user.

This strategy is crucial for maximizing the accuracy and utility of the automated matching process, reducing the manual effort required by the user.
