# Feature Build Log

---

## [FEAT-003]: [Feature Title]
**ID:** FEAT-003
**Status:** Pending
**Dependencies:** [e.g., FEAT-001 (User Auth), Database Schema v1]
**Files Impacted:** [To be updated by Agent]

### 1. User Story
* **As a** [type of user]
* **I want to** [perform action]
* **So that** [achieve value]

### 2. Acceptance Criteria (AC)
#### A. Functional Requirements
* [ ] AC 1: [Specific behavior]
* [ ] AC 2: [Specific behavior]

#### B. UI/UX States (Required)
* [ ] **Success:** [What happens when it works?]
* [ ] **Loading:** [Visual feedback during async calls.]
* [ ] **Error:** [Validation messages for invalid inputs.]
* [ ] **Empty:** [What shows if there is no data?]

#### C. Technical Validation
* [ ] Feature must pass existing unit tests.
* [ ] Responsive design verified (Mobile/Desktop).

### 3. Agent Build Notes
*(Agent: Log key changes, new routes, or logic decisions here for future reference.)*

---

## [Archive / Completed Features]
> (Move completed features here to keep the active context window clean.)

### [FEAT-002]: Modal View for new Menu button. 
**ID:** FEAT-002
**Status:** Completed
**Dependencies:** None
**Files Impacted:** `features.md`, `index.html`, `menstruation-hygiene.html`, `adolescence-young-boys.html`, `cervical-cancer-awareness.html`

#### 1. User Story
* **As a** user
* **I want to** click on a 'Menu' button
* **So that** I can select the relevant topic slides from a pop-up modal screen in the middle. 

#### 2. Acceptance Criteria (AC)
##### A. Functional Requirements
* [x] AC 1: A sticky 'Menu' button centered in the top-middle which replaces the old navigation bar across all .html pages (`index.html`, `menstruation-hygiene.html`, `adolescence-young-boys.html`, `cervical-cancer-awareness.html`). 
* [x] AC 2: When users clicks on the 'Menu' button, a pop-up modal screen appears in the middle of the screen, which is titled, 'Select your topic', and has the topics listed in square boxes (3 in a row for Desktop and 2 in a row for Mobile), which are mainly - 'Cervical Cancer Quiz' (linked to `index.html`), 'Cervical Cancer Awareness' (linked to `cervical-cancer-awareness.html`), 'Menstruation Health' (linked to `menstruation-hygiene.html`), and 'Adolescence in Boys' (linked to `adolescence-young-boys.html`).
* [x] AC 3: User clicking on the square tabs will lead the user to the selected tab's relevant HTML page. 
* [x] AC 4: User should have the ability to scroll in the modal, if more topics are added in the near future. 
* [x] AC 5: The modal will also have a simple 'X' button on the top-right corner, which will exit the modal and return the user to the topic currently selected. 

##### B. UI/UX States (Required)
* [x] **Success:** When the 'Menu' button (should have 3 horizontal lines stacked as an icon) is clicked, the modal appears, in the middle of the screen, on both Desktop and Mobile, and blurs and darkens the slide in the background, making it seem as if the modal is being popped out towards the user. The square tabs are simple and neat, and should display the topics in a clear manner, with a 1 line description (10 words or less). The topic heading should be 50% larger than the description, and the description should be in a light font as compared to the bold of the topic heading. The entire design of the modal should be neat, user-friendly, and minimalistic. 

##### C. Technical Validation
* [x] Responsive design verified (Mobile/Desktop). Make sure the modal view has appropriate amount of rows based on the screen size on hand (3 in a row for Desktop and 2 in a row for Mobile).

#### 3. Agent Build Notes
*(Agent: Log key changes, new routes, or logic decisions here for future reference.)*
- Replaced the legacy navigation bar with a new `#menu-btn` (hamburger style) fixed element in all four HTML pages.
- Added the `nav-modal` overlay containing the grid of topics mapping to corresponding HTML endpoints.
- Used CSS Grid (`repeat(3, 1fr)` -> `repeat(2, 1fr)`) to cleanly enforce 3 columns on Desktop and 2 columns on Mobile for the tile layout.
- Implemented `.modal-overlay` with `backdrop-filter: blur(8px)` and semi-transparent background to generate the focus/pop-out effect requested.
- Bound JS functions `openModal()` and `closeModal(event)` with `stopPropagation()` to cleanly handle opening, and exiting via the "X" or clicking the backdrop boundary.

### [FEAT-001]: .txt Stubs to Slide Decks (.html pages)
**ID:** FEAT-001
**Status:** Completed
**Dependencies:** None
**Files Impacted:** `menstruation-hygiene.html`, `adolescence-young-boys.html`, `cervical-cancer-awareness.html`, `features.md`

#### 1. User Story
* **As a** regular user who arrives at this app
* **I want to** see an informative slide deck (.html page) with 7-10 slides which has pulled context from the stubs (.txt) in the working directory
* **So that** I can learn more about the required topic. 

#### 2. Acceptance Criteria (AC)
##### A. Functional Requirements
* [x] AC 1: Users should be able to click a 'Next' or 'Previous' Button to go ahead or back.

##### B. UI/UX States (Required)
* [x] **Success:** Simple forward and backward navigation buttons for slides. 

##### C. Technical Validation
* [x] Responsive design verified (Mobile/Desktop).

#### 3. Agent Build Notes
*(Agent: Log key changes, new routes, or logic decisions here for future reference.)*
- Created `menstruation-hygiene.html`, `adolescence-young-boys.html`, and `cervical-cancer-awareness.html`.
- Added a global navigation bar menu to each page linking to the 4 topics: "Cervical Cancer Quiz", "Cervical Cancer Awareness", "Menstruation Health", and "Adolescence in Boys" as per PRD spec.
- Implemented clean, minimal and playful presentation styling with responsive CSS (grid/flex). Theme variables distinctively adapted to fit each topic (e.g. Blue colors for boys, Pinks for girls/hygiene).
- Built Vanilla JS functions to seamlessly handle "Next", "Previous" and keyboard support mapping (Arrow keys and Spacebar).
- Embedded the `.txt` content logically into structured HTML slide cards context.