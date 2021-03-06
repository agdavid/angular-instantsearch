---
title: Widgets - Hits
layout: widget.pug
---

# Hits

## Description

Displays a list of hits.
sYou can use the directive `<ng-template></ng-template>` to customize.

## Code example

```html
<ng-ais-hits>
  <ng-template
    let-hits="hits"
    let-results="results"
  >
    <!-- No results message -->
    <div *ngIf="hits.length === 0">
      No results found matching <strong>{{results.query}}</strong>.
    </div>

    <!-- Hit template -->
    <div *ngFor="let hit of hits">
      <h1>
        <ng-ais-highlight
          attribute="title"
          [hit]="hit"
        >
        </ng-ais-highlight>
      </h1>

      <p>{{hit.description}}</p>
    </div>
  </ng-template>
</ng-ais-hits>
```
