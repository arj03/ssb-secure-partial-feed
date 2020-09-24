# SSB secure partial feed

A set of methods to enable and verify a feed for secure partial replication

Uses [ssb-observables](https://github.com/arj03/ssb-observables)

## Verify(msgId, messages, latestSeqForFeed)

Uses ssb-observables to get the latest state of msgId. Then uses messages & latestSeqForFeed to verify against the latest state.

## VerifyFeed(feedId, latestSeqForFeed, contactMessages, profileMessages)

Finds the two messages for partial contact & profile state. Then uses contactMessages and profileMessages together with `verify`.

## EnablePartial(feedId)

Creates two messages for partial contact & profile state if they don't exists and stores the current state for each of those.

## HasPartial(feedId)

Checks if a profile has created the two messages for partial contact & profile state.

## UpdatePartial(feedId)

Ensures that the state of contact and profile is current with the feed.
