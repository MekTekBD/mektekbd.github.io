---
layout: post
title:  "MicroController 1"
date:   2017-03-28
desc: "MicroController 1"
keywords: "mektek"
categories: [microcontroller]
tags: [microcontroller]
icon: icon-html
---


Basic Microcontroller: পর্ব – ১<br>
বর্তমান সময়ের অন্যতম আলোচনার বিষয় হল স্মার্ট সিস্টেম বানানো, অর্থাৎ যে সিস্টেম স্বয়ংক্রিয়ভাবে ইনপুট এবং সেন্সিং প্রক্রিয়ার মাধ্যমে আউটপুট কন্ট্রোল করতে পারে। তাই বর্তমান সময়ে এরকম ডিভাইস এর প্রয়োজনীয়তা এখন অনেক যেখানে ডিভাইস একইসাথে ইনপুট নেওয়ার , সেন্স করার , প্রসেসিং করা এবং সেই অনুযায়ী আউটপুট দেওয়ার ক্ষমতা রাখে।<br><br>



   <!-- ![edit]({{ site.img_path }}/3steps/edit.gif) -->
	<center><img src="{{ site.img_path }}/mc.png" width="500px" height="400px"><center><br><br><br>



 মাইক্রোকন্ট্রোলার সেরকমই একটা ডিভাইস । যদি একবাক্যে বলা হয় , তাহলে মাইক্রোকনট্রোলার মানে হল একটা সিংগেল চিপ্স কম্পিউটার। একটা কম্পিউটার এর যেমন র্যাম , রোম , হার্ডডিস্ক এবং বিভিন্ন পেরিফেরাল কমিউনিকেশন প্রটোকল আছে তেমন একটা মাইক্রোকন্ট্রোলার এর ও র্যাম , রোম এবং বিভিন্ন কমিউনিকেশন সিস্টেম আছে। কথাগুলা মনে হয় নতুনদের জন্য একটু কঠিন লাগবে । তাই মুল কথা হল , একটা মাইক্রোকন্ট্রোলার মানে একটা সিঙ্গেল চিপ্স কম্পিউটার। এটা মনে করলেই পুরা বিষয়টা সহজ লাগবে।

এখন কিছু প্রশ্ন থাকতে পারে , যে আমাদের কাছে এতবড় মাল্টিপ্রসেসিং ক্ষমতা সম্পন্ন কম্পিউটার থাকতে আমরা কেন মাইক্রোকন্ট্রোলার ব্যাবহার করব । কিংবা মাইক্রোকন্ট্রোলার এর প্রোগ্রামিং শিখেই বা কি লাভ। বিষয়টা একটা উদাহরন এর মাধ্যমে ভালভাবে বোঝা যাবে। ধরা যাক , আমার বাসায় একটা পানির ট্যাংক আছে। সেটাতে একটা মটর ব্যাবহার করা হয় পানি তোলার জন্য । এখন পুরা সিস্টেমটাকে যদি আমি অটোমেটিক করতে চাই অর্থাৎ ট্যাংকে পানি ভর্তি হলেই মটর বন্ধ হয়ে যাবে আর একটা নির্দিষ্ট লেভেল নিচে নামলে মটর অন হয়ে যাবে। তাহলে সেখানে নিশ্চয় একটা কন্ট্রোলিং সিস্টেম লাগবে। সেক্ষেত্রে আমাদের পাম্প কন্ট্রোলের জন্য একটা কম্পিউটার ফিক্সড করে দেওয়া অনেক বেশি ব্যায়বহুল আর অসুবিধাজনক, যেখানে একটা একশ টাকা দামের বা তার চেয়েও কম দামের মাইক্রোকন্ট্রলার দিয়ে সহজেই সিস্টেমটা কন্ট্রোল করা যায়। আমার মনে হয় এবার বিষয়টা অনেক বেশি পরিষ্কার ।

আরেকটা বিষয় অনেক ক্ষেত্রে কনফিউশন ঘটায়। সেটা হল মাইক্রোপ্রসেসর আর মাইক্রোকন্ট্রোলার। মাইক্রোপ্রসেসর আর মাইক্রোকন্ট্রোলার কিন্তু এক বিষয় না। মাইক্রোপ্রসেসরের সাথে র্যাম , রোম ইত্যাদি যোগ করে একটা কম্পিউটার বানানো হয় । অপরদিকে মাইক্রোকন্ট্রোলার নিজেই একটা এক প্রসেসিং ইউনিটের কম্পিউটার । সীমাবদ্ধতা হল কন্ট্রোলারের প্রসেসিং ক্ষমতা , প্রসেসরের প্রসেসিং ক্ষমতার চেয়ে কম ।

যারা একেবারেই নতুন তাদের অনেকের প্রশ্ন থাকতে পারে যে , কন্ট্রোলার কিভাবে চালায় বা এর প্রোগ্রামিং ল্যাংগুয়েজই বা কি। বিষয়টা অনেকটা পরিসরের উপর নির্ভরশীল । মানে বিভিন্ন ব্রান্ডের কনট্রোলার এর জন্য বিভিন্ন প্লাটফর্ম থাকতে পারে । তবে ইউনিভার্সাল ভাবে বলা যায় সব কন্ট্রোলারের ব্রান্ডগুলাই সি এবং এসেম্বলি সাপোর্টেড এনভারনমেন্ট রাখে তাদের কন্ট্রোলারে প্রোগ্রামিং এর জন্য। আরেকটা বিষয় মাইক্রোকন্ট্রোলারে যে প্রোগ্রাম আপলোড দেয়া হয় তা কিন্তু হেক্সাডেসিমেল কোডে থাকে । তাই যে ল্যাংগুয়েজেই কোড করা হোক না কেন তা থেকে হেক্সা কোডে কনভার্ট করতে হবে।

এখন কথা হল কি দিয়ে কোড মাইক্রোকন্ট্রোলারে আপলোড করা হয় বা কিভাবে কোড হয় , সেটা জানার আগে আমাদের মাইক্রোকন্ট্রোলার এর কিছু ভাগের উপর খেয়াল রাখতে হবে। Microchips কম্পানির PIC সিরিজ আর Atmel কোম্পানির AVR সিরিজের মাইক্রোকন্ট্রোলার বেশী ব্যাবহার করা হয়। আমরা মাইক্রোকন্ট্রোলারের আরও কিছু প্রকারভেদ দেখার পর মুল কোডিং এ যাব।

প্রথমত ডেটা রেজিস্টার এর উপর ভিত্তি করে মাইক্রোকন্ট্রোলার কে বেশ কয়েকভাগে ভাগ করা যায় । তবে এখানে ডেটা রেজিস্টার বলতে কোন ইলেকট্রিক রোধ কে বোঝানো হচ্ছে না । ডেটা রেজিস্টার বলে মেমরি কে বোঝানো হচ্ছে। মাইক্রোকন্ট্রোলার এর ভেতরে বিভিন্ন রেজিস্টার আছে যেগুলা দিয়ে আমাদের সেগুলাকে ইন্সট্রাকশন দিতে পারি। কিভাবে দিতে হবে তা আমরা পরে দেখব।

বেসিকালি মাইক্রোকন্ট্রোলার গুলা ৮ বিট , ১৬ বিট , ২৪ বিট , ৩২ বিট এবং বর্তমানে ৬৪ বিট এর ও কিছু মাইক্রোকন্ট্রোলার পাওয়া যায়। অর্থাৎ এদের যে একটা ডেটা রেজিস্টার তার বিট সংখার উপর ভিত্তি করে এই ভাগ টা করা হয়েছে। আমরা বেসিক মাইক্রোকন্ট্রোলার সিরিজে ৮ বিট Atmel সিরিজর মাইক্রোকন্ট্রোলার গুলা নিয়ে আলোচনা করব।

এখন দেখা যাক কিছু প্রতিষ্ঠিত মাইক্রোকন্ট্রোলার ম্যানুফ্যাকচারিং কোম্পানি এবং তাদের কন্ট্রোলার সমন্ধে। তাহলে আমাদের পরবর্তিতে এগুলা ব্যাবহার করতে সুবিধা হবে।

Atmel: বর্তমান সময়ে অন্যতম জনপ্রিয় কন্ট্রোলার গুলার মধ্যে একটা হল এটমেল কোম্পানির Avr সিরিজ। সাধারনত মাইক্রোকন্ট্রোলার এর নাম না শুনলেও আরডুইনোর নামটা অনেকেরই জানা । হুটহাট ছোট খাটো প্রজেক্ট থেকে শুরু করে বড় বড় প্রজেক্টও আরডুইনোতে খুব সহজে করা যায়। বেসিকালি আরডুইনোকে ডেভলপ করা হয়েছে open source হিসেবে। অর্থাৎ এর দ্বারা করা কোড এবং অন্যান্য অনেক বিষয় যেমন লাইব্রেরি, সফটওয়ার বিনামুল্যে বিতরনযোগ্য। এছাড়া Atmel কোম্পানির অন্যান্য কন্ট্রোলার গুলা হল 32-bit AVR® UC3 microcontroller, megaAVR MCU, Xmega MCU, Atiny series ইত্যাদি । Atmel এর মাইক্রকন্ট্রোলার গুলা দামে কিছুটা কম । অনেক তথ্য সমৃদ্ধ ডেটাশিট একে অনেক বেশি জনপ্রিয় করেছে। এতে কোড করার জন্য Atmel কোম্পানির Atmel Studio সবার জন্য উন্মুক্ত করা হয়েছে। এখানে অনেক লাইব্রেরী বানানোই আছে । লাইব্রেরী জিনিষটা কি যাদের প্রোগ্রামিং সমন্ধে ধারনা আছে তারা বুঝতে পারবে। না বুঝলেও সমস্যা নাই পরে আস্তে আস্তে বোঝা যাবে। এছাড়া যেসব সফটওয়্যার আছে সেগুলা হল WinAvr, Eclipes, CodeBlocks, Micro C ইতাদি। এগুলা সগুলাই মোটামুটিভাবে সি এবং সি++ ব্যাবহার করে প্রোগ্রাম করার জন্য। আমরা এই সিরিজে WinAvr কে ব্যাবহার করব প্রোগ্রামিং এর জন্য। আজকের পর্বটা এখানেই শেষ।

পর্ব – ২ এ আমরা আরও কিছু মাইক্রোকন্ট্রোলার সমন্ধে জেনে প্রোগ্রামিং এ যাব এবং কিভাবে একটা ছোট টুনিবাল্ব মাইক্রোকন্ট্রোলার দিয়ে জ্বালানো যায় তা দেখব।