Sure, here's the revised version without the dropdowns:

I've constructed this **CCBP Timeline** application utilizing the principles we've covered thus far.

### Reference Image:
  
  ![CCBP Timeline Output](https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-output.gif)

### Design Files:

  - [Extra Small (Size < 576px) and Small (Size >= 576px)](https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-sm-output-v2.png)
  - [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px)](https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-lg-output.png)

### Setup Instructions:

  - Download dependencies by running `npm install`.
  - Start up the app using `npm start`.

### Completion Instructions:

  - The app incorporates the following functionalities:
    - Initially, the page displays the timeline items list using **Chrono custom rendering** based on the `categoryId`.
    - The `TimelineView` component is provided with `timelineItemsList`, consisting of a list of timeline item objects with the following properties:
      - For `timelineItemObject` with `categoryId` as `COURSE`:
        | Key           | Data Type |
        | ------------- | --------- |
        | id            | String    |
        | categoryId    | String    |
        | title         | String    |
        | courseTitle   | String    |
        | description   | String    |
        | duration      | String    |
        | tagsList      | Array     |
      - For `tagsListObject`:
        | Key           | Data Type |
        | ------------- | --------- |
        | id            | String    |
        | name          | String    |
      - For `timelineItemObject` with `categoryId` as `PROJECT`:
        | Key           | Data Type |
        | ------------- | --------- |
        | id            | String    |
        | categoryId    | String    |
        | title         | String    |
        | projectTitle  | String    |
        | description   | String    |
        | imageUrl      | String    |
        | duration      | String    |
        | projectUrl    | String    |
    - If the `categoryId` value in `timelineItemObject` is `PROJECT`, a Project card is rendered, including:
      - A **Visit** link. Clicking on it navigates the page to the respective project.
      - A **Calendar** icon with the respective `duration` text.
    - If the `categoryId` value in `timelineItemObject` is `COURSE`, a Course card is rendered, including:
      - A **Clock** icon with the respective `duration` text.
    - The timeline items list data is provided as a value to the `items` prop for the `Chrono` component from **react-chrono**, so the title is displayed beside each card.

### Components Structure:

  ![Component Structure Breakdown](https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-component-structure-breakdown.png)

### Implementation Files:

  These files were utilized for the implementation:
  - `src/components/TimelineView/index.js`
  - `src/components/TimelineView/index.css`
  - `src/components/CourseTimelineCard/index.js`
  - `src/components/CourseTimelineCard/index.css`
  - `src/components/ProjectTimelineCard/index.js`
  - `src/components/ProjectTimelineCard/index.css`

### Important Note:

  - I referred to the [React Chrono](https://learning.ccbp.in/frontend-development/course?c_id=2f4192f7-7495-49ca-a6ce-6b74005e25f1&s_id=a152928a-64cc-4697-936c-db2e3c4f2716&t_id=416f0cab-8425-413b-9157-c7b4d4ae4467) reading material for this project.
  - For clock and calendar icons in the cards, I utilized `AiFillClockCircle` and `AiFillCalendar` icons from `react-icons`, respectively.

### Resources:

  - Colors:
    - Hex: #171f46
    - Hex: #1e293b
    - Hex: #ffffff
    - Hex: #0967d2
    - Hex: #2b237c

  - Font-families:
    - Roboto
