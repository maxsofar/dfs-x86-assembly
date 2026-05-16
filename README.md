# DFS in x86 Assembly

Depth-first search implemented in x86 Assembly, under strict register constraints.

## Background

This started as a mandatory assignment in a low-level systems course at the Technion. Partway through, it was reclassified as an optional bonus after a significant portion of the class couldn't complete it. I did.

## The challenge

The interesting part isn't DFS itself — it's doing it in Assembly with a limited number of available registers.

DFS requires tracking visited nodes and managing a call stack for recursive traversal. In a high-level language you get variables, data structures, and a call stack for free. In x86 Assembly with register constraints, you have to be deliberate about every byte: what goes in a register, what gets pushed to the stack, when to save and restore state, and how to avoid clobbering values mid-traversal.

## What it does

- Reads a graph from memory
- Traverses it depth-first, tracking visited nodes
- Outputs the traversal order

## Stack

x86 Assembly (32-bit), written and tested on Linux with NASM.

## Course context

**234118** — Introduction to Computer Organization, Technion.  
The DFS task was one component of a larger assignment. This repo contains only the DFS implementation.
