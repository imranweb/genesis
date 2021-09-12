---
id: component-library
title: Component Library
sidebar_label: Component Library
---

Our recommendation is to create components within the libs/ui-kit folder.

All the components in the libs/ui-kit should be presentational components receiving all their data as props.

While we follow the atomic design pattern while designing components we strongly discourage creating a folder structure for atoms and molecules (Teams never seem to reach a consensus of whether a component should go inito the atoms or molecules folder). A single flat level folder structure makes it easy to view all components in the project.

## Generating the storybook for your components

```
nx g @nrwl/react:storybook-configuration ui-kit
```

To run the story book

```
yarn nx serve ui-kit:storybook
```

Reference
https://www.youtube.com/watch?v=sFpqyjT7u4s
