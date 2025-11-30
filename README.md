# 🎬 Kids Video Library

A safe, curated video library for kids - accessible from any device! Browse channels, watch videos, and keep everything organized in one kid-friendly interface.

**🌐 Live App:** [https://pbatalion.github.io/kids-video-app/](https://pbatalion.github.io/kids-video-app/)

## ✨ Features

### For Kids
- 🎨 **Beautiful Interface** - Colorful, easy-to-navigate design
- 📺 **Channel Cards** - Browse videos organized by channel
- 🎥 **Safe Viewing** - YouTube links blocked to prevent app-switching
- 📱 **Works Everywhere** - Phone, tablet, computer - any device with a browser
- 🔒 **No YouTube Access** - Can't navigate to YouTube from embedded videos

### For Parents (Admin Mode)
- 🧮 **Math Challenge Lock** - Solve a simple math problem to access admin features
- 🔍 **Channel Search** - Search YouTube channels by name, no need to find IDs
- 📺 **Import Channels** - Add entire channels (up to 50 recent videos)
- ➕ **Add Individual Videos** - Manually add specific videos
- 🔄 **Refresh Channels** - Update channels with latest videos from YouTube
- 🗑️ **Delete Channels** - Remove entire channels with one click
- 💾 **Export/Import Library** - Share your library across devices
- 🎯 **Delete Individual Videos** - Remove videos you don't want

## 🚀 Quick Start

### For Viewing (Kids)
1. Go to [https://pbatalion.github.io/kids-video-app/](https://pbatalion.github.io/kids-video-app/)
2. Click a channel card to see videos
3. Click a video to watch
4. Click "Back to Channels" to choose another channel

### For Managing (Parents)
1. Click the ⚙️ icon in the top-right corner
2. Solve the math challenge (changes each time)
3. Use the admin panel to:
   - **Import Channel** - Search for channels or enter a channel ID
   - **Add Video** - Add individual videos by URL
   - **Export Library** - Download your collection as JSON
   - **Import Library** - Load a saved library
4. Each channel card shows:
   - **🔄 Refresh** - Update with latest videos (or "Enable Refresh" to set up)
   - **🗑️ Delete** - Remove the entire channel
5. Click "Exit Admin" when done

## 📖 How To Use

### Adding a New Channel

**Method 1: Search (Easiest)**
1. Enter admin mode (⚙️ → solve math)
2. Click "📺 Import Channel"
3. Type the channel name (e.g., "Bluey", "Peppa Pig")
4. Press Enter or click "🔍 Search"
5. Click the channel you want from results
6. Click "Import"

**Method 2: Channel ID**
1. Find the channel on YouTube
2. Copy the channel ID from the URL
3. Enter admin mode
4. Click "📺 Import Channel"
5. Paste the ID in "Enter Channel ID Manually"
6. Click "Import"

### Syncing Across Devices

Your library is stored in your browser's localStorage. To use the same library on multiple devices:

1. On device 1: Enter admin mode → "💾 Export Library"
2. Save the JSON file
3. On device 2: Enter admin mode → "📁 Import Library"
4. Select the JSON file

You can also use cloud storage (Dropbox, Google Drive, etc.) to keep the JSON file synced and import it when needed.

### Refreshing a Channel

If a channel has new episodes:

1. Enter admin mode
2. Find the channel card
3. Click "🔄 Refresh" (or "🔍 Enable Refresh" if it's an old channel)
4. Confirm the refresh
5. The channel will update with the latest 50 videos

### YouTube Link Blocking

The app prevents kids from clicking:
- YouTube logo (top of video)
- "Watch on YouTube" button (bottom-right corner)

All other video controls (play, pause, volume, fullscreen) work normally.

## 🔧 Technical Details

- **No Backend** - Completely client-side, hosted on GitHub Pages
- **YouTube Data API v3** - For importing channels and searching
- **localStorage** - Stores your video library in the browser
- **No Installation** - Just visit the URL
- **No Login Required** - Works immediately
- **Offline Ready** - Once loaded, the app works without internet (videos require internet)

## 🎯 Use Cases

- **Home Media Hub** - Curate safe content for your kids
- **Classroom** - Teachers can create educational video collections
- **Waiting Rooms** - Businesses can set up kid-friendly viewing stations
- **Family Sharing** - Export/import to share collections with family

## 🔒 Privacy & Security

- ✅ All data stored locally in your browser
- ✅ No user accounts or personal information
- ✅ No tracking or analytics
- ✅ YouTube API key is public (intentional for family use)
- ✅ Math challenge prevents accidental admin access
- ⚠️ API key is exposed in source code (acceptable for personal/family use)

## 🛠️ Customization

Want to change something? The entire app is in `index.html` - just edit and push to GitHub:

- **Math Challenge Difficulty** - Change the number ranges in `showMathChallenge()`
- **Videos Per Channel** - Change `maxResults=50` in `importChannel()`
- **Channel Card Size** - Modify `.channel-grid` CSS
- **Colors** - Update the gradient in `body` CSS

## 📱 Browser Support

Works on:
- ✅ Chrome, Edge, Brave (desktop & mobile)
- ✅ Safari (desktop & mobile/iPad)
- ✅ Firefox (desktop & mobile)
- ✅ Any modern browser with localStorage support

## 🐛 Troubleshooting

**"No channels yet!"**
- You need to import at least one channel
- Click ⚙️ → solve math → "Import Channel"

**Videos won't play**
- Check your internet connection
- Video might be age-restricted or region-blocked
- Try refreshing the channel to get newer videos

**"Enable Refresh" instead of "Refresh"**
- Click it once to detect the channel ID
- After that, the refresh button will work

**Library disappeared**
- Browser cache/localStorage was cleared
- Import your exported library backup if you have one

**Search not finding channels**
- Make sure the channel name is spelled correctly
- Try searching part of the name
- Some channels might not appear in search results

## 🎨 Screenshots

### Main View (Channel Cards)
Beautiful grid showing all your imported channels with thumbnails and video counts.

### Channel Videos
Click a channel to see all its videos in an embedded player.

### Admin Panel
Math challenge protection and powerful management tools.

## 📄 License

This is a personal/family project. Feel free to fork and customize for your own use!

## 🙏 Credits

Built with:
- YouTube Data API v3
- GitHub Pages
- Love for making kid-friendly tech ❤️

---

**Made with ❤️ for safe, accessible kids' content**
