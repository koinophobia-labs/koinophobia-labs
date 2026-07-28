# You Know Ball

**Status:** TestFlight builds accepted; external validation pending  
**Role:** Founder, product owner, product engineer, and final approver

## The problem

Sports conversation is full of strong opinions but weak feedback. Most products reward volume, reactions, or gambling activity instead of the quality of the argument.

You Know Ball turns a take into a structured debate:

> Drop a take. Defend your argument. Prove you know ball.

## The product loop

1. Receive or choose a sports take.
2. Select the argument lane.
3. Defend the take against BanterBot.
4. Receive scoring and feedback tied to the argument.
5. Review the receipt, rematch with context, and improve.

## Product systems

- SwiftUI application with franchise persistence and tolerant decoding
- argument coverage lanes and scoring-trust rules
- novelty decay to reduce repetitive bot behavior
- Daily Take, streak, replay, Film Room, and Ball Receipt systems
- sport-parity classification and contextual rematches
- shareable results designed around the argument rather than a wagering outcome

## Safety boundary

The product can discuss sports, teams, players, performance, and arguments. It is not designed to recommend wagers, optimize a bet, encourage chasing losses, or turn sports analysis into gambling influence.

An internal 80-prompt adversarial campaign produced **0 hard wagering violations in the tested scope**. That result belongs to the evaluated build and rubric; it is not a claim of universal safety. See the [red-team casebook](red-team-casebook.md).

## Current evidence

- TestFlight builds 26 and 27 accepted
- scoring, persistence, rematch, Daily Take, receipt, and sharing systems implemented
- device and regression testing completed across the release slices
- external tester count remains zero, so retention and replayability are not yet proven

## Next proof

- put the product in front of outside sports fans
- measure whether users finish debates and choose to rematch
- inspect false-positive and false-negative scoring behavior
- continue adversarial wagering and conversational-drift testing

