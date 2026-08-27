# FIXGO Backend

Spring Boot REST API for the FIXGO vehicle assistance marketplace. See the root [README.md](../README.md) for the overall project and folder-structure rationale.

## 1. Stack

| Component | Choice |
|---|---|
| Language | Java |
| Framework | Spring Boot |
| Build tool | Maven |
| Database | PostgreSQL (Supabase free tier initially) |
| Auth | Email/password first; OTP later |

## 2. Structure

Modular by business domain (`auth`, `user`, `vehicle`, `provider`, `job`, `rating`, `report`, `notification`, `admin`), each with `controller` / `service` / `repository` / `entity` / `dto` sub-packages, plus shared `config` and `common`. See the root README's [Backend Structure](../README.md#3-backend-structure-backend) section for the full tree.

## 3. Getting Started

_To be added once the Maven project (`pom.xml`) is scaffolded — this folder currently holds the target package structure only._

## 4. Conventions

- New features get their own domain package, not a shared `services`/`controllers` package.
- Keep entities, DTOs and repositories inside their owning domain — cross-domain reads go through that domain's service, not its repository.
