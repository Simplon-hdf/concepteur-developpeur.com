# Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Linter != Debugger](#linter--debugger)
- [Most popular Linters](#most-popular-linters)
  - [JSLint](#jslint)
  - [JSHint](#jshint)
  - [ESLint](#eslint)
  - [Benchmark](#benchmark)
- [Get started with ESLint](#get-started-with-eslint)
  - [Initialisation](#initialisation)

# Introduction

A linter is a program which anaylize in **real time** code written by a developper, to prevent of potentials error can occured, as call to non existing function for example.

Linters can be configured to work in some context as following :

- In the code editor
- In a shared code process (As in GitHub for example)
- In a terminal manually triggered by a command, or automatically before transpilation 

# Linter != Debugger

Linter and Debugger are 2 distincts programs, linter will manage errors during edidion (before transpilation or compilation), the debbuger will manage errors during compilation / transpilation process, it will permit to identificate other kind of errors whose are ignored by linter.

Debbuger can provide more detailed informations on errors and bring some process obsvervation, like call stack for example.

# Most popular Linters

## JSLint

JSLint is a ready to use linter, right after installation. 
It do not requires configuration, but therefore, it do not allow you to define personnalized rules.
Error logging can be kinda weird.

## JSHint

JSHint is a ready to use linter, right after installation. 
It do not requires configuration, but therefore, it do not allow you to define personnalized rules.
Error logging can be kinda weird.

## ESLint

## Benchmark

# Get started with ESLint

## Initialisation