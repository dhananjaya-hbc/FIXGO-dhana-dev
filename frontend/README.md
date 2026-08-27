# FIXGO Frontend

React Native app for the FIXGO vehicle assistance marketplace, targeting Android and iOS from a single codebase. See the root [README.md](../README.md) for the overall project and folder-structure rationale.

## 1. Stack

| Component | Choice |
|---|---|
| Framework | React Native, TypeScript |
| UI Components | shadcn-style component system (`react-native-reusables` + NativeWind/Tailwind) |
| Maps | OpenStreetMap + Leaflet |
| Push Notifications | Firebase Cloud Messaging |

## 2. Structure

Feature-first under `src/features/` (`auth`, `customer`, `provider`, `admin`, `job`, `rating`, `notifications`), shared shadcn-style primitives in `src/components/ui`. See the root README's [Frontend Structure](../README.md#4-frontend-structure-frontend) section for the full tree.

## 3. Getting Started

_To be added once the React Native project is scaffolded — `android/` and `ios/` currently hold placeholders and will be populated by the RN tooling (`npx react-native init` or equivalent)._

## 4. Conventions

- Keep customer, provider and admin flows in separate `features/` folders even where UI overlaps.
- Only cross-feature, reusable UI belongs in `src/components`; feature-specific UI stays inside that feature's folder.
- Shared API calls live in `src/services/api`, not inline in screens/components.
