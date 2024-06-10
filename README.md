I've built this **CCBP Timeline** application using the concepts we have learned so far.

### Refer to the image below:

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-output.gif" alt="ccbp timeline output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

### Design Files

<details>
<summary>Click to view</summary>

- [Extra Small (Size < 576px) and Small (Size >= 576px)](https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-sm-output-v2.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px)](https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-lg-output.png)

</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Completion Instructions

<details>
<summary>Functionality included</summary>
<br/>

The app includes the following functionalities:

- Initially, the page displays the timeline items list using **Chrono custom rendering** based on the `categoryId`.
- The `TimelineView` component is provided with `timelineItemsList`. It consists of a list of timeline item objects with the following properties:

  - The `timelineItemObject` with `categoryId` as `COURSE` has the following properties:

    |     Key     | Data Type |
    | :---------: | :-------: |
    |     id      |  String   |
    | categoryId  |  String   |
    |    title    |  String   |
    | courseTitle |  String   |
    | description |  String   |
    |  duration   |  String   |
    |  tagsList   |   Array   |

  - The `tagsListObject` has the following properties:

    | Key  | Data Type |
    | :--: | :-------: |
    |  id  |  String   |
    | name |  String   |

  - The `timelineItemObject` with `categoryId` as `PROJECT` has the following properties:

    |     Key      | Data Type |
    | :----------: | :-------: |
    |      id      |  String   |
    |  categoryId  |  String   |
    |    title     |  String   |
    | projectTitle |  String   |
    | description  |  String   |
    |   imageUrl   |  String   |
    |   duration   |  String   |
    |  projectUrl  |  String   |

- If the value of the key `categoryId` in `timelineItemObject` is `PROJECT`, then a Project card is rendered.
  - The `ProjectTimelineCard` consists of a **Visit** link. When a user clicks on it, the page navigates to the respective project.
  - The `ProjectTimelineCard` consists of a **Calendar** icon with the respective `duration` text.
- If the value of the key `categoryId` in `timelineItemObject` is `COURSE`, then the Course card is rendered.
  - The `CourseTimelineCard` consists of a **Clock** icon with the respective `duration` text.
- The timeline items list data is provided as a value to the `items` prop for the `Chrono` component from **react-chrono**, so the title is displayed beside each card.

</details>

<details>
<summary>Components Structure</summary>

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/ccbp-timeline-component-structure-breakdown.png" alt="component structure breakdown" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

</details>

<details>
<summary>Implementation Files</summary>
<br/>

These files were used to complete the implementation:

- `src/components/TimelineView/index.js`
- `src/components/TimelineView/index.css`
- `src/components/CourseTimelineCard/index.js`
- `src/components/CourseTimelineCard/index.css`
- `src/components/ProjectTimelineCard/index.js`
- `src/components/ProjectTimelineCard/index.css`
</details>

### Important Note

<details>
<summary>Click to view</summary>

<br/>

- To build this project, I referred to the <a href='https://learning.ccbp.in/frontend-development/course?c_id=2f4192f7-7495-49ca-a6ce-6b74005e25f1&s_id=a152928a-64cc-4697-936c-db2e3c4f2716&t_id=416f0cab-8425-413b-9157-c7b4d4ae4467' target="_blank">React Chrono</a> reading material.

**The following instructions are required for the tests to pass:**

- `AiFillClockCircle` and `AiFillCalendar` icons from `react-icons` are used for **clock** and **calendar** icons in the cards, respectively.

</details>

### Resources

<details>
<summary>Colors</summary>

<br/>

<div style="background-color: #171f46; width: 150px; padding: 10px; color: white">Hex: #171f46</div>
<div style="background-color: #1e293b; width: 150px; padding: 10px; color: white">Hex: #1e293b</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #0967d2; width: 150px; padding: 10px; color: white">Hex: #0967d2</div>
<div style="background-color: #2b237c; width: 150px; padding: 10px; color: white">Hex: #2b237c</div>

</details>

<details>
<summary>Font-families</summary>

- Roboto

</details>

> ### _Things to Keep in Mind_
>
> - All components you implement should go in the `src/components` directory.
> - Don't change the component folder names as those are the files being imported into the tests.
> - **Do not remove the pre-filled code**.
> - Want to quickly review some of the concepts you’ve been learning? Take a look at the Cheat Sheets.