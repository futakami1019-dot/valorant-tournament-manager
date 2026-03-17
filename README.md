# VALORANT Community Tournament Manager

This project is a small tool designed to help manage community VALORANT tournaments.

It is used during custom game tournaments to automatically retrieve match results using the Riot Games API and store the results in a Google Spreadsheet for tournament management.

## Purpose

The purpose of this tool is to automate match result recording during small community tournaments. Instead of manually writing down player statistics after each match, the organizer can retrieve match data directly from the Riot API.

The tool is intended for small community events and is not a public service.

## Features

- Retrieve match data from Riot Games API
- Automatically record match results into Google Sheets
- Track player statistics such as:
  - ACS (Average Combat Score)
  - Kills
  - Deaths
  - Assists
  - Team results
  - Round wins
- Track match IDs and tournament match order

## Tournament Format

The tool is currently designed for small community tournaments with approximately 40 participants.

Example format:

- 4 teams
- Single elimination bracket
- Semifinals
- Third place match
- Final match

Each match is played as a custom game in VALORANT.

## How It Works

1. The tournament organizer enters Riot IDs of players in a Google Spreadsheet.
2. A Google Apps Script retrieves the player's PUUID using the Riot Account API.
3. The script retrieves the latest match ID using the VALORANT Matchlist API.
4. The script retrieves detailed match data using the VALORANT Match Details API.
5. Player statistics are written into the spreadsheet automatically.

The organizer manually triggers the script after each match finishes.

## APIs Used

This project uses the following Riot Games APIs:

- Riot Account API
- VALORANT Matchlist API
- VALORANT Match Details API

The tool respects Riot API rate limits and only requests match data when the tournament organizer triggers the script.

## Usage Scope

This project is used only for small community tournament management and is not intended for large-scale public services.

Typical usage:

- Community tournaments
- Local esports events
- Private competitions

## Disclaimer

This project is not affiliated with or endorsed by Riot Games.

This tool does not provide a public API or allow third-party access.
