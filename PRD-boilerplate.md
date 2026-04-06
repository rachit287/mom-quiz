# Product Requirement Document: [Project Name]

## 1. Context & North Star
* **The Story:** [Short narrative of the product's evolution.]
* **Current Objective:** [The primary goal of the current development cycle.]
* **Target Audience:** [Who is using this, and what is their tech literacy?]

## 2. Global Technical Constraints (The "How")
> **Note to AI Agent:** Adhere strictly to these standards for every feature build.
* **Tech Stack:** [e.g., Next.js 14, TypeScript, Tailwind CSS, Prisma]
* **Coding Standards:** [e.g., Use functional components, Atomic Design pattern, shadcn/ui components.]
* **State Management:** [e.g., Zustand for global state, React Query for server state.]
* **Error Handling:** [e.g., Every API call must have a catch block and a user-facing Toast notification.]

## 3. Introduction (The Why)
* **High-Level Features:** [Summary of the epic's scope.]
* **Success Metrics:** [KPIs like "Reduce checkout time by 20%".]
* **Reference Links:** [Links to API docs, Figma, or Legal requirements.]

## 4. Design Principles & Global States
* **Consistency:** All new components must pull from `@/components/ui`.
* **Standard States:** Every interactive feature **must** account for:
    1. **Loading:** Skeleton screens or spinners.
    2. **Empty:** Guidance text when no data exists.
    3. **Error:** Helpful feedback and "try again" actions.

## 5. Engineering Requirements (Infrastructure)
* **Security:** [e.g., All routes must be protected by middleware.]
* **Performance:** [e.g., Images must use next/image for optimization.]
* **Persistence:** [e.g., LocalStorage vs. Database rules.]