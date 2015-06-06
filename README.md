=============================
Djangocon Subtitles Indexings
=============================

The problem
===========

On the one hand, we have the DjangoCon videos on Youtube and on the
other hand, the transcript of the talks provided by the Speech To Text
translators. We'd like to make subtitles.

The solution
============

This proof of concept :

 - Downloads the automatic Youtube captions for a given video
 - Matches each block of subtitle to its equivalent in the transcripts using DiffLib
 - Produces a Subtitles files ready for re-uploading

What we need to do
==================
 - Take it a step further and upload the RST back to Youtube (easy).
 - Create a proper command line tool that, given a Youtube video id (or link) and its .txt
   transcript, does it all
 - Create a Django App to do the same thing AND manage OAuth2 properly. For now, one has
   to copy-paste manually the token.

Why this may be useless but still
=================================

Youtube actually provides this functionnality ("sync=true" in the insert API,
similar on the website) but I'm an expert for discovering this sort of things after writing
the code.

What you'll find in the source
==============================

A proof of concept ipython notebook. and the srt files produced.

