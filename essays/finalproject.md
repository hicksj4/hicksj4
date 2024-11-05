---
layout: essay
type: essay
title: "Final Project Idea"
# All dates must be YYYY-MM-DD format!
date: 2024-11-25
published: true
labels:
  - Final Project
---

## Project: ArtShare (Working Title)

## Overview

The problem: Many university students possess artistic talents across various disciplines such as music, visual arts, design, and more. However, there is no centralized platform tailored to the university community where they can showcase their work in one space. Existing social media platforms are either too broad or not conducive to fostering a local artistic community within the campus.

The solution: ArtShare is a web application designed exclusively for university students to share short snippets of their creative works. It features a scrollable feed where users can view posts and like them fostering interaction and collaboration among student artists. Essentially a spinoff idea of Campus Jam project, but with a more Instagram/Tiktok approach to the feed page. Will utilizie Soundcloud embedding to play the music without redirecting to the site, staying centralized on the ArtShare feed.

## Approach

ArtShare allows students to:

    Create Profiles: Students can sign up using their university credentials to create a profile that includes their artistic interests, bio, and a portfolio of their works.

    Share Creative Works: Users can upload images of their artwork or embed links to external media (e.g., SoundCloud tracks, YouTube videos) showcasing their music or performance pieces. Each post can include a description and tags for better discoverability.

    Engage with Content: The platform features a scrollable feed where users can view posts from others, like, and comment to provide feedback and encouragement.

    Discover Artists: Users can search for and filter posts by categories such as art form, genre, or tags. This helps them find content and creators that match their interests.

    Admin Oversight: Administrators monitor the platform for inappropriate content, manage categories and tags, and ensure the community remains respectful and supportive.

Technical Stack:

    Frontend: Next.js (React) with Bootstrap 5 for responsive design.
    Backend: Node.js with Express.js.
    Database: PostgreSQL for storing user profiles, posts, comments, and likes.
    Hosting: Deployed on DigitalOcean, utilizing DigitalOcean Spaces for media storage.

## Mockup Pages Ideas

Landing Page:

    Introduction to ArtShare with a call-to-action to sign up or log in.

User Home Page (Feed):

    Scrollable feed displaying recent posts from all users or tailored to the user's interests.
    "Load More" button to fetch additional posts.

Profile Page:

    Displays user's profile picture, bio, artistic interests, and their posts.
    Option to edit profile information.

Post Creation Page:

    Form for creating a new post with fields for description, tags, and media upload or embed link.

Post Detail Page:

    Displays the post's media content, description, and likes count.
    Allows users to 'like'/'heart' the post.

Search and Discovery Page:

    Search bar and filters to find posts or artists by category, tags, or keywords.

Admin Dashboard:

    Accessible only to administrators.
    Tools for monitoring content, managing users, and updating categories and tags.

## Beyond the Basics

Notifications:

    Real-time notifications for likes and new followers.

Comment Functionality:

    Allow users to leave comments on posts.
