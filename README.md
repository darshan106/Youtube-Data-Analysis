1. **Clone the Repository:**
   First, clone the repository to your local machine:
   ```sh
   git clone https://github.com/darshan106/youtube-data-analysis.git
   ```

2. **Navigate to the Project Directory:**
   ```sh
   cd Youtube-Data-Analysis
   ```

3. **Create and Activate a Virtual Environment:**
   Create a virtual environment to manage your project dependencies:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

4. **Install Dependencies:**
   Install the required Python libraries listed in the `requirements.txt` file:
   ```sh
   pip install -r requirements.txt
   ```

5. **Obtain YouTube API Key:**
   Obtain a YouTube API key from the [Google Developer Console](https://console.developers.google.com/). Enable the YouTube Data API v3 for your project.

6. **Open the Jupyter Notebook:**
   Start the Jupyter Notebook server:
   ```sh
   jupyter notebook
   ```

   Open the `TamilTechChannels-Analysis.ipynb` notebook in your browser.

7. **Add Your YouTube API Key:**
   In the Jupyter Notebook, locate the cell where the API key is set and replace `'YOUR_API_KEY'` with your actual API key.

8. **Execute the Notebook Cells:**
   Run each cell sequentially by clicking on the cell and pressing `Shift + Enter` or by using the "Run" button in the toolbar.

## Analysis and Explanation

### 1. Import Libraries
   The required libraries for data manipulation, visualization, and API interaction are imported.

### 2. Set Up YouTube API
   - The YouTube API client is set up using the provided API key.
   - A list of channel IDs is defined for which data will be retrieved.

### 3. Get Channel Status
   - The `get_channel_status` function retrieves basic statistics about each channel, including the number of subscribers, views, total videos, and the playlist ID for uploaded videos.
   - This data is stored in a Pandas DataFrame.

### 4. Get Video IDs
   - The `get_video_ids` function fetches all video IDs from each channel's upload playlist.
   - This is done to gather detailed information for each video.

### 5. Get Video Details
   - The `get_video_details` function retrieves detailed information for each video, such as title, published date, view count, like count, comment count, and duration.
   - The data is cleaned and converted to appropriate types.

### 6. Categorize Video Duration
   - Video durations are categorized into 'Short (<1m)', 'Medium (1m - 1h)', and 'Long (>1h)' for easier analysis.

### 7. Average Likes and Comments
   - The average number of likes and comments per video for each channel is calculated.
   - Bar plots are generated to visualize these averages, providing insights into audience engagement.

### 8. Scatter Plots of Views vs. Likes and Comments
   - Scatter plots are created to analyze the relationship between views and likes/comments for each channel.
   - This helps in understanding the engagement pattern for different types of videos.

### 9. Calculate and Plot Engagement Rate
   - The engagement rate is calculated as the sum of likes and comments divided by the number of views.
   - A bar plot visualizes the average engagement rate for each channel, highlighting how engaging the content is.

### 10. Monthly Video Upload Frequency
   - The number of videos uploaded each month is counted for each channel.
   - A line plot shows the monthly upload frequency, providing insights into the content production schedule.

### 11. Generate and Plot Word Clouds
   - Word clouds are generated for video titles and descriptions of each channel.
   - This visualizes the most common words used, giving an idea of the content themes.

### Summary of Analysis
- **Channel Performance:** The overall performance of each channel is analyzed in terms of subscribers, views, and video count.
- **Engagement Metrics:** Insights into audience engagement are gained by examining likes, comments, and engagement rates.
- **Content Themes:** Word clouds help identify common themes and keywords in video titles and descriptions.
- **Upload Patterns:** Monthly upload frequency analysis reveals the consistency and scheduling of content production.

By following these steps and running the notebook, you can perform a comprehensive analysis of multiple YouTube channels, gaining valuable insights into their performance and content strategies.
