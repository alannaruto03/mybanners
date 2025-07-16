# Chinese Homework Buddy - App Design Document

## 📱 App Overview
**Target Users**: Non-Chinese-speaking parents helping Year 1 kids with Chinese homework
**Main Goal**: Make Chinese homework accessible and manageable for non-Chinese families
**Key Differentiator**: Word-level pinyin/English alignment with pronunciation and vocabulary building

---

## 🎨 Main Screen Wireframe

```
┌─────────────────────────────────────┐
│  📚 Chinese Homework Buddy          │
│                               ⚙️📋   │
├─────────────────────────────────────┤
│                                     │
│         📷 SCAN HOMEWORK            │
│      ┌─────────────────────┐        │
│      │                     │        │
│      │    [Camera Icon]    │        │
│      │   Tap to scan new   │        │
│      │     homework        │        │
│      │                     │        │
│      └─────────────────────┘        │
│                                     │
│  📖 Recent Homework                 │
│  ┌─────────────────────────────────┐ │
│  │ 📄 Dec 15 - Math Worksheet     │ │
│  │ 📄 Dec 14 - Reading Practice   │ │
│  │ 📄 Dec 13 - Character Writing  │ │
│  └─────────────────────────────────┘ │
│                                     │
│  📝 My Word List (23 words)         │
│  ┌─────────────────────────────────┐ │
│  │ 学习 xuéxí - to study          │ │
│  │ 老师 lǎoshī - teacher          │ │
│  │ 作业 zuòyè - homework          │ │
│  └─────────────────────────────────┘ │
│                                     │
├─────────────────────────────────────┤
│   📖   📚   ⭐   📋   👨‍👩‍👧‍👦        │
│  Scan  Words Star History Profile  │
└─────────────────────────────────────┘
```

---

## 🔄 User Journey & App Flow

### Primary Flow: Scanning Homework

```
1. SCAN → 2. PROCESS → 3. VIEW → 4. INTERACT → 5. SAVE

┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐
│ Camera  │ => │ OCR +   │ => │ Display │ => │ Toggle  │ => │ Save    │
│ Capture │    │ Process │    │ Result  │    │ Modes & │    │ Words & │
│         │    │         │    │         │    │ Listen  │    │ History │
└─────────┘    └─────────┘    └─────────┘    └─────────┘    └─────────┘
```

### Scanning Screen Wireframe

```
┌─────────────────────────────────────┐
│  ← Chinese Homework Buddy           │
├─────────────────────────────────────┤
│                                     │
│  ┌─────────────────────────────────┐ │
│  │                                 │ │
│  │        CAMERA VIEWFINDER        │ │
│  │                                 │ │
│  │     [Auto-focus rectangle]      │ │
│  │                                 │ │
│  │                                 │ │
│  └─────────────────────────────────┘ │
│                                     │
│         💡 TIPS:                    │
│   • Hold steady for best results   │
│   • Ensure good lighting           │
│   • Keep text horizontal           │
│                                     │
│  ┌─────────┐  ┌─────────┐  ┌───────┐ │
│  │   📁    │  │   📷    │  │  ⚡   │ │
│  │ Gallery │  │ Capture │  │ Flash │ │
│  └─────────┘  └─────────┘  └───────┘ │
└─────────────────────────────────────┘
```

### Text Display & Interaction Screen

```
┌─────────────────────────────────────┐
│ ← Chinese Homework Buddy       📤📑 │
├─────────────────────────────────────┤
│ Toggle View:                        │
│ ┌───┐┌─────┐┌───┐┌─────────┐        │
│ │中 ││拼音 ││英 ││拼音+英  │        │
│ └───┘└─────┘└───┘└─────────┘        │
│                               🔊📖  │
├─────────────────────────────────────┤
│                                     │
│  今天的作业是学习中文               │
│  jīntiān de zuòyè shì xuéxí zhōngwén│
│  Today's homework is learning Chinese│
│                                     │
│  [长按 'xuéxí' - highlighted]       │
│  ┌─────────────────────┐             │
│  │ 📝 Save to Word List│             │
│  │ 🔊 Pronounce        │             │
│  │ ❌ Cancel           │             │
│  └─────────────────────┘             │
│                                     │
│  请完成第一页到第三页。             │
│  qǐng wánchéng dì yī yè dào dì sān yè│
│  Please complete pages 1 to 3.     │
│                                     │
└─────────────────────────────────────┘
```

---

## 🎯 Complete Feature Breakdown

### Core Features

#### 📷 **Scan & Translate**
- **Photo Capture**: High-quality camera integration
- **OCR Engine**: Extract Chinese text with high accuracy
- **Translation Engine**: Instant Chinese to English translation
- **Image Enhancement**: Auto-crop, brightness adjustment
- **Processing Indicator**: Clear progress feedback

#### 🔤 **Pinyin/English Overlay Toggle**
- **四种显示模式** (4 Display Modes):
  - **[中]**: Original Chinese only - clean, focused view
  - **[拼音]**: Chinese + pinyin below each character/word
  - **[英]**: Chinese + English translation below
  - **[拼音+英]**: Chinese + pinyin + English (three-line format)
- **Word-Level Alignment**: Pinyin and English matched to specific words
- **Smart Segmentation**: Automatic word boundary detection
- **Instant Toggle**: Switch modes without re-processing

#### 🔊 **Text-to-Speech (TTS)**
- **Tap to Hear**: Individual word or sentence pronunciation
- **Speed Control**: Slow/Normal/Fast playback
- **Repeat Function**: Loop difficult words
- **High-Quality Voice**: Native Mandarin pronunciation
- **Read All**: Play entire homework aloud

#### 📝 **Vocabulary Builder**
- **Long Press to Save**: Intuitive word selection
- **Word Cards**: Chinese character + pinyin + English + example
- **Local Storage**: Words saved offline for review
- **Study Mode**: Flashcard-style review system
- **Progress Tracking**: Words learned, review streaks

#### 📚 **History Management**
- **Homework Archive**: All scanned pages saved
- **Quick Access**: Thumbnail view with dates
- **Re-edit Capability**: Reopen and modify translations
- **Search Function**: Find specific homework by content
- **Organization**: Sort by date, subject, or difficulty

### Advanced Features

#### 👨‍👩‍👧‍👦 **Parent/Child Modes**
- **Parent Mode**: Full translations + teaching tips
- **Child Mode**: Pinyin-only for independent practice
- **Progress Sharing**: Parents see child's vocabulary growth
- **Difficulty Adjustment**: Gradual reduction of translation assistance

#### 🎨 **Visual Design Elements**
- **Color Coding System**:
  - Chinese characters: Black (#000000)
  - Pinyin: Blue (#1976D2) 
  - English: Gray (#666666)
- **Font Optimization**: Kid-friendly, large, clear fonts
- **Intuitive Icons**: Universally recognized symbols
- **Consistent Spacing**: Easy reading for young eyes

#### 🔔 **Smart Reminders**
- **Daily Vocabulary Review**: Gentle push notifications
- **Homework Scan Reminders**: Based on school schedule
- **Progress Celebrations**: Milestone achievements
- **Customizable Timing**: Respect family routines

---

## 🛠️ Recommended Tech Stack

### **Framework**: Flutter 3.x
- **Why**: Single codebase for iOS/Android
- **Performance**: Native-like performance
- **UI Flexibility**: Custom designs for parent+child appeal
- **Community**: Extensive plugin ecosystem

### **OCR & ML**: Google ML Kit
```yaml
dependencies:
  google_mlkit_text_recognition: ^0.8.0
  google_mlkit_translation: ^0.8.0
```
- **Offline OCR**: Works without internet
- **High Accuracy**: Excellent Chinese character recognition
- **Free Tier**: Cost-effective for initial users

### **Text-to-Speech**: Flutter TTS
```yaml
dependencies:
  flutter_tts: ^3.8.3
```
- **Multi-language Support**: Mandarin Chinese + English
- **Platform Integration**: Native iOS/Android TTS engines
- **Speed Control**: Adjustable playback rate

### **Local Storage**: Hive + SharedPreferences
```yaml
dependencies:
  hive: ^2.2.3
  hive_flutter: ^1.1.0
  shared_preferences: ^2.2.2
```
- **Hive**: Fast local database for word lists
- **SharedPreferences**: User settings and app state
- **Offline-First**: Full functionality without internet

### **Camera & Image Processing**
```yaml
dependencies:
  camera: ^0.10.5
  image_picker: ^1.0.4
  image: ^4.1.3
```

### **UI Enhancement**
```yaml
dependencies:
  animations: ^2.0.8
  lottie: ^2.7.0
  google_fonts: ^6.1.0
```

---

## 🎨 Design Principles

### **Parent-Friendly Design**
- **Large Touch Targets**: Easy finger navigation
- **Clear Visual Hierarchy**: Important actions stand out
- **Minimal Cognitive Load**: Simple, focused interfaces
- **Error Prevention**: Confirm destructive actions

### **Child-Friendly Elements**
- **Playful Colors**: Warm, encouraging palette
- **Achievement System**: Stars, badges, progress bars
- **Simple Navigation**: Bottom tab bar with icons
- **Immediate Feedback**: Visual/audio confirmation

### **Accessibility**
- **High Contrast**: Text readable in all lighting
- **Font Scaling**: Respect system accessibility settings
- **Voice Over Support**: Screen reader compatibility
- **Color Blind Friendly**: Not dependent on color alone

---

## 🚀 Unique Value Propositions

### **vs Google Lens**
1. **Word-Level Alignment**: Pinyin/English matched to specific words
2. **Pronunciation Learning**: Tap any word to hear correct Mandarin
3. **Vocabulary Building**: Save and review unknown words
4. **Parent Context**: Explanations designed for non-Chinese speakers
5. **Offline Capability**: Works without internet connection
6. **Educational Focus**: Learning-oriented, not just translation

### **vs Traditional Dictionary Apps**
1. **Homework Context**: Understands classroom assignments
2. **Visual Learning**: See characters in context, not isolation
3. **Family Workflow**: Designed for parent-child collaboration
4. **Progress Tracking**: Monitor vocabulary growth over time

---

## 📊 Development Phases

### **Phase 1 - MVP (4-6 weeks)**
- Basic camera capture
- OCR text extraction
- Simple translation display
- Basic word saving

### **Phase 2 - Core Features (6-8 weeks)**
- Toggle view modes
- TTS implementation
- History management
- Word list with review

### **Phase 3 - Polish (4-6 weeks)**
- Parent/Child modes
- Notifications system
- UI/UX refinements
- Performance optimization

### **Phase 4 - Advanced (6-8 weeks)**
- Smart word segmentation
- Advanced study features
- Analytics and insights
- Community features

---

## 🎯 Success Metrics
- **User Engagement**: Daily active usage by families
- **Learning Outcomes**: Vocabulary retention rates
- **Parent Satisfaction**: Confidence in helping with homework
- **Child Independence**: Reduced reliance on translation over time

---

*This design document provides a comprehensive foundation for building Chinese Homework Buddy - an app that bridges the language gap for non-Chinese-speaking families while fostering independent learning in young students.*