# Travel Destination Finder

A Python GUI application built with Tkinter that helps users find ideal travel destinations based on selected preferences. The app filters and ranks destinations from a CSV dataset based on features like climate, activities, and popularity.

## Features

- GUI built using Tkinter
- Preference-based destination filtering
- Popularity-based ranking
- Fallback suggestions when no match is found
- Easy-to-extend CSV data format

## How It Works

1. Load travel destinations from a CSV file.
2. User selects preferences such as "tropical", "adventure", "shopping", etc.
3. The app filters destinations that match selected features.
4. Displays top 5 destinations sorted by popularity.
5. If no match is found, fallback to top 5 most popular destinations.

## CSV File Format

The CSV file (travel_destinations.csv) should include the following headers:
