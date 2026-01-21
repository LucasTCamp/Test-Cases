

# TikTok Video Test Cases

---

## Test Case 1

**Test Case ID:** TTK_UPLOAD_001  
**Title:** Verify if upload feature is successful with valid MOV video format  
**Requirement:** The system must accept MOV format videos within size and length limits.  
**Test Type:** POSITIVE  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- Valid test video file (MOV) is available on device  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Make post public  
5. Verify video preview loads  
6. Tap "Next"  
7. Add caption: "Test upload"  
8. Tap "Post"  

### Test Data
- **File:** `test_video.mov`  
- **Format:** MOV  
- **Size:** 21MB  
- **Length:** 67 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "Test upload"  

### Expected Result
- Video uploads successfully  
- Processing screen appears  
- Video appears in user’s profile  
- Video is playable by user/others  
- Caption displays correctly  

**Priority:** High (core part of TikTok)

---

## Test Case 2

**Test Case ID:** TTK_UPLOAD_002  
**Title:** Verify if upload feature is successful with valid MPEG video format  
**Requirement:** The system must accept MPEG format videos within size and length limits.  
**Test Type:** POSITIVE  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- Valid test video file (MPEG) is available on device  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video2.mpeg`  
4. Make post public  
5. Verify video preview loads  
6. Tap "Next"  
7. Add caption: "Test upload"  
8. Tap "Post"  

### Test Data
- **File:** `test_video.mpeg`  
- **Format:** MOV  
- **Size:** 67MB  
- **Length:** 21 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "Test upload 2"  

### Expected Result
- Video uploads successfully  
- Processing screen appears  
- Video appears in user’s profile  
- Video is playable by user/others  
- Caption displays correctly  

**Priority:** High (core part of TikTok)

---

## Test Case 3

**Test Case ID:** TTK_INVALID_VIDEO_LENGTH_001  
**Title:** Verify if upload feature fails for videos under minimum length  
**Requirement:** Any video being uploaded must be 3 seconds or more  
**Test Type:** NEGATIVE  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User has a video under 3 seconds to upload  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Short_video.mp4`  
4. Verify system denies the upload  
5. Verify the system informs the user of the mistake  

### Test Data
- **File:** `Short_video.mp4`  
- **Format:** MP4  
- **Size:** 67MB  
- **Length:** 2 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "Test invalid video length (Short)"  

### Expected Result
- Video upload fails  
- System informs user of mistake and video requirements  
- System allows user to return to posting or profile  

**Priority:** Medium

---

## Test Case 4

**Test Case ID:** TTK_INVALID_VIDEO_LENGTH_002  
**Title:** Verify if upload feature fails for videos exceeding maximum length  
**Requirement:** Any video being uploaded has a maximum limit of 10 minutes (600 seconds)  
**Test Type:** NEGATIVE  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User has a video over 10 minutes  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Long_video.mp4`  
4. Verify system denies the upload  
5. Verify the system informs the user of the mistake  

### Test Data
- **File:** `Long_video.mp4`  
- **Format:** MP4  
- **Size:** 287MB  
- **Length:** 287 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "Test invalid video length (Long)"  

### Expected Result
- Video upload fails  
- System informs user of mistake and requirements  
- System allows user to return to posting or profile  

**Priority:** High

---

## Test Case 5

**Test Case ID:** TTK_VIDEO_SIZE_BOUNDARY_001  
**Title:** Verify if videos within size boundary limits can be uploaded  
**Requirement:** Any video being uploaded must be ≤ 287MB  
**Test Type:** Boundary  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User has a video that is exactly 287MB  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Boundary_video.mp4`  
4. Verify system accepts the upload  
5. Verify video preview loads  
6. Tap "Next"  
7. Add caption: "Test upload"  
8. Tap "Post"  

### Test Data
- **File:** `Boundary_video.mp4`  
- **Format:** MP4  
- **Size:** 287MB  
- **Length:** 287 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "Make sure videos right on the limit size can be posted (287MB)"  

### Expected Result
- Processing screen appears  
- Video appears in user’s profile  
- Video is playable by user  
- Caption displays correctly  

**Priority:** Medium

---

## Test Case 6

**Test Case ID:** TTK_VIDEO_LENGTH_BOUNDARY_001  
**Title:** Verify if videos at minimum length boundary can be uploaded  
**Requirement:** Any video being uploaded must be exactly 3 seconds  
**Test Type:** Boundary  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User has a video exactly 3 seconds long  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Boundary_Length_video.mp4`  
4. Verify system accepts the upload  
5. Verify video preview loads  
6. Tap "Next"  
7. Add caption: "Test upload"  
8. Tap "Post"  

### Test Data
- **File:** `Boundary_Length_video.mp4`  
- **Format:** MP4  
- **Size:** 4MB  
- **Length:** 3 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  

### Expected Result
- Processing screen appears  
- Video appears in user’s profile  
- Video is playable by user  
- Caption displays correctly  

**Priority:** Medium

---

## Test Case 7

**Test Case ID:** TTK_EMPTY_CAPTION_001  
**Title:** Verify if videos with no caption can be uploaded  
**Requirement:** Captions may be empty (0 characters minimum)  
**Test Type:** Edge  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User uploads a video without a caption  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Edge_video.mp4`  
4. Verify system accepts the upload  
5. Verify video preview loads  
6. Tap "Next"  
7. Leave caption empty  
8. Tap "Post"  

### Test Data
- **File:** `Edge_video.mp4`  
- **Format:** MP4  
- **Size:** 67MB  
- **Length:** 67 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  

### Expected Result
- Processing screen appears  
- Video appears in user’s profile  
- Video is playable by user  
- Video uploads without caption  

**Priority:** High

---

## Test Case 8

**Test Case ID:** TTK_MAXIMUM_HASHTAGS_001  
**Title:** Verify if videos with maximum allowed hashtags can be uploaded  
**Requirement:** System allows 0–30 hashtags  
**Test Type:** Edge  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User uploads a video with 30 hashtags  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Edge_video.mp4`  
4. Verify system accepts the upload  
5. Verify video preview loads  
6. Tap "Next"  
7. Add caption with 30 hashtags  
8. Tap "Post"  

### Expected Result
- Processing screen appears  
- Video appears in user’s profile  
- Video is playable by user  

**Priority:** High

---

## Test Case 9

**Test Case ID:** TTK_OVER_MAX_CAPTION_CHARACTERS_001  
**Title:** Verify system behavior for captions over maximum character limit  
**Requirement:** Maximum of 2,200 caption characters  
**Test Type:** Blackbox  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User uploads a video with caption over 2,200 characters  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Blackbox_1_video.mp4`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption exceeding 2,200 characters  
7. Tap "Post"  

### Expected Result
- Video processing occurs  
- Video uploads without caption or system prevents caption submission  

**Priority:** High

---

## Test Case 10

**Test Case ID:** TTK_PROHIBITED_CONTENT  
**Title:** Verify prohibited content cannot be uploaded  
**Requirement:** Content policy enforcement (violence, nudity, hate speech, etc.)  
**Test Type:** Blackbox  

### Preconditions
- User is logged into TikTok  
- User has navigated to upload screen  
- User uploads a video with prohibited content  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `Blackbox_2_video.mp4`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption with prohibited content  
7. Tap "Post"  

### Expected Result
- System detects policy violation  
- Video is removed or blocked  
- User is informed of the violation  

**Priority:** High
