import React, { useState, useEffect, useMemo } from 'react';
import { 
  Zap, Shield, User, Heart, TrendingUp, 
  Crown, Compass, Briefcase, Share2, 
  Calculator, Sparkles, MessageSquare, Loader2, RefreshCw, 
  BarChart3, Settings, UserPlus, Info, Calendar,
  LineChart, Target, Edit3, Mars, Venus, Printer, MessageCircle,
  FileText, Activity, Hash, Binary, ChevronRight, Layout, Binary as BinaryIcon,
  PackageCheck
} from 'lucide-react';

/**
 * App - 战略级生命密码矩阵 v3.4 (WhatsApp 战略打包增强版)
 * 适配：阿盛 (Castor)
 * AI 顾问：波 (Bo)
 * 核心升级：
 * 1. 强化 WhatsApp 分享内容，生成更专业的“战略摘要包”。
 * 2. 优化了 PDF 导出时的渲染深度，确保文字边缘锐利。
 * 3. 整合了 Money (宠物猫) 的元素作为“情绪平衡项”建议。
 */

const App = () => {
  // --- 核心计算引擎 ---
  const reduceNum = (n) => {
    if (!n) return 0;
    let num = Math.abs(parseInt(n));
    while (num > 9) {
      num = String(num).split('').reduce((acc, curr) => acc + parseInt(curr), 0);
    }
    return num;
  };

  const calculateFullMatrix = (y, m, d, analysisYear) => {
    const dStr = String(d).padStart(2, '0');
    const mStr = String(m).padStart(2, '0');
    const yStr = String(y);
    
    const d1 = parseInt(dStr[0]) || 0; const d2 = parseInt(dStr[1]) || 0;
    const m1 = parseInt(mStr[0]) || 0; const m2 = parseInt(mStr[1]) || 0;
    const yr1 = parseInt(yStr[0]) || 0; const yr2 = parseInt(yStr[1]) || 0;
    const yr3 = parseInt(yStr[2]) || 0; const yr4 = parseInt(yStr[3]) || 0;

    const A = reduceNum(d1 + d2); 
    const B = reduceNum(m1 + m2); 
    const C = reduceNum(reduceNum(yr1 + yr2) + reduceNum(yr3 + yr4)); 

    const D = reduceNum(A + B); 
    const E = reduceNum(B + C); 
    const F = reduceNum(D + E); 

    const G = reduceNum(A + D); 
    const H = reduceNum(C + E); 
    const I = reduceNum(D + F); 
    const J = reduceNum(E + F); 
    const K = reduceNum(I + J); 

    const personalYear = reduceNum(parseInt(analysisYear) + reduceNum(m) + reduceNum(d));

    return { 
      A, B, C, D, E, F, G, H, I, J, K, personalYear,
      steps: [
        { label: '天赋根底', id: 'A', val: A, formula: `日(${dStr})` },
        { label: '情感驱动', id: 'B', val: B, formula: `月(${mStr})` },
        { label: '外部环境', id: 'C', val: C, formula: `年(${yStr})` },
        { label: '性格左轴', id: 'D', val: D, formula: 'A + B' },
        { label: '性格右轴', id: 'E', val: E, formula: 'B + C' },
        { label: '主命格数', id: 'F', val: F, formula: 'D + E', highlight: true },
        { label: '坐镇核心', id: 'K', val: K, formula: 'I + J', highlight: true }
      ]
    };
  };

  // --- 状态管理 ---
  const [profile, setProfile] = useState({
    name: 'Castor 阿盛',
    gender: 'Male',
    birthYear: 1980,
    birthMonth: 9,
    birthDay: 30,
    targetYear: 2026 
  });
  
  const [isEditingName, setIsEditingName] = useState(false);
  const [aiLoading, setAiLoading] = useState(false);
  const [aiResponse, setAiResponse] = useState('');
  const [chatInput, setChatInput] = useState('');

  const results = useMemo(() => {
    return calculateFullMatrix(profile.birthYear, profile.birthMonth, profile.birthDay, profile.targetYear);
  }, [profile.birthYear, profile.birthMonth, profile.birthDay, profile.targetYear]);

  const flowYears = [2024, 2025, 2026, 2027, 2028, 2029, 2030];
  const birthYears = Array.from({ length: 80 }, (_, i) => 1950 + i);
  const months = Array.from({ length: 12 }, (_, i) => i + 1);
  const days = Array.from({ length: 31 }, (_, i) => i + 1);

  // --- AI 接口逻辑 ---
  const callGemini = async (prompt, systemPrompt = "") => {
    setAiLoading(true);
    const apiKey = ""; 
    const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
    
    const body = {
      contents: [{ parts: [{ text: prompt }] }],
      systemInstruction: { parts: [{ text: systemPrompt }] }
    };

    const fetchResult = async (retries = 3, delay = 1000) => {
      try {
        const response = await fetch(url, {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify(body)
        });
        const data = await response.json();
        if (!response.ok) throw new Error(data.error?.message || "API Error");
        return data.candidates?.[0]?.content?.parts?.[0]?.text;
      } catch (err) {
        if (retries > 0) {
          await new Promise(r => setTimeout(r, delay));
          return fetchResult(retries - 1, delay * 2);
        }
        throw err;
      }
    };

    try {
      const text = await fetchResult();
      const safeText = typeof text === 'object' ? JSON.stringify(text) : String(text || "");
      setAiResponse(safeText);
    } catch (err) {
      setAiResponse(`Terminal Error: ${err.message}`);
    } finally {
      setAiLoading(false);
    }
  };

  const handleAiAnalyze = () => {
    if (!results) return;
    const prompt = `对象: ${profile.name}(${profile.gender})。命格: ${results.F}-${results.K}。流年: ${profile.targetYear}年 (流年数 ${results.personalYear})。请生成一份整齐的报告，包含性格深度分析、股票投资风险评估及青训项目落地建议。`;
    const system = "你是一位精通生命密码的私人战略顾问。请使用清晰的 Markdown 标题分节回答。";
    callGemini(prompt, system);
  };

  const handleChat = () => {
    if (!chatInput.trim() || !results) return;
    const prompt = `分析指令: ${chatInput}。当前背景: 主命数 ${results.F}, 坐镇 ${results.K}。`;
    const system = "你是波 (Bo)，一个专业且严谨的命理战略顾问。";
    callGemini(prompt, system);
    setChatInput('');
  };

  // --- WhatsApp 打包分享逻辑 ---
  const handleWhatsAppShare = () => {
    const aiSnippet = aiResponse ? aiResponse.substring(0, 100) + "..." : "详见 PDF 报告。";
    const message = encodeURIComponent(
      `📑 *${profile.name} 战略决策简报包* 📑\n` +
      `----------------------------------\n` +
      `👤 对象: ${profile.name} (${profile.gender === 'Male' ? '男' : '女'})\n` +
      `🔢 主命格: ${results.F} 号人 (爆发力先锋)\n` +
      `🔒 坐镇码: ${results.K} (内层驱动核心)\n` +
      `📅 分析年份: ${profile.targetYear}\n` +
      `⚡ 流年势能: ${results.personalYear} (${results.personalYear === 4 ? '系统架构年' : '能量变动年'})\n` +
      `----------------------------------\n` +
      `💡 AI 战略摘要: ${aiSnippet}\n` +
      `----------------------------------\n` +
      `>>> 详细图表与方程式请查阅随附 PDF 报告。报告由 Bo AI 战略核心生成。`
    );
    window.open(`https://wa.me/?text=${message}`, '_blank');
  };

  const numMap = {
    1: { name: "领袖", color: "bg-orange-500", text: "text-orange-400" },
    2: { name: "沟通", color: "bg-blue-400", text: "text-blue-400" },
    3: { name: "创意", color: "bg-rose-500", text: "text-rose-400" },
    4: { name: "策划", color: "bg-emerald-500", text: "text-emerald-400" },
    5: { name: "方向", color: "bg-cyan-500", text: "text-cyan-400" },
    6: { name: "智慧", color: "bg-amber-400", text: "text-amber-400" },
    7: { name: "人缘", color: "bg-purple-500", text: "text-purple-400" },
    8: { name: "责任", color: "bg-slate-700", text: "text-slate-400" },
    9: { name: "梦想", color: "bg-indigo-500", text: "text-indigo-400" }
  };

  return (
    <div className="min-h-screen bg-[#02050a] text-slate-200 p-4 md:p-8 font-sans selection:bg-indigo-500/30">
      <div className="max-w-5xl mx-auto flex flex-col gap-6">
        
        {/* Top Header - 打印隐藏 */}
        <div className="flex justify-between items-center border-b border-white/5 pb-6 no-print">
          <div className="flex items-center gap-4">
            <div className="p-3 bg-indigo-600/20 border border-indigo-500/30 rounded-2xl">
              <PackageCheck className="text-indigo-400 animate-pulse" size={24} />
            </div>
            <div>
              <h1 className="text-xl font-black tracking-tight text-white uppercase italic">Strategic Matrix Terminal</h1>
              <p className="text-[10px] text-slate-500 font-mono tracking-widest uppercase">Report Packaging Mode Active</p>
            </div>
          </div>
          <div className="flex gap-2">
            <button onClick={handleWhatsAppShare} className="p-3 rounded-2xl bg-emerald-600/20 border border-emerald-500/30 text-emerald-400 hover:bg-emerald-600 hover:text-white transition-all shadow-lg" title="分享摘要包至 WhatsApp">
              <MessageCircle size={20} />
            </button>
            <button onClick={() => window.print()} className="p-3 rounded-2xl bg-indigo-600 text-white shadow-lg hover:bg-indigo-500 transition-all scale-105" title="导出报告 PDF">
              <Printer size={20} />
            </button>
            <button onClick={() => setIsEditingName(!isEditingName)} className={`p-3 rounded-2xl border transition-all ${isEditingName ? 'bg-indigo-600 border-indigo-400 text-white' : 'bg-slate-900 border-white/10 text-slate-400'}`}>
              <Edit3 size={20} />
            </button>
          </div>
        </div>

        {/* 打印页眉 */}
        <div className="hidden only-print text-center border-b-4 border-slate-900 pb-8 mb-10">
          <h1 className="text-3xl font-black text-slate-900 uppercase tracking-widest">生命密码全相位战略执行报告</h1>
          <div className="flex justify-center gap-12 mt-4 text-xs font-bold text-slate-600 uppercase">
            <span>Subject: {profile.name}</span>
            <span>Target Cycle: {profile.targetYear}</span>
            <span>Ref: CAST-ALPHA-{new Date().getFullYear()}</span>
          </div>
        </div>

        {/* 输入面板 - 打印隐藏 */}
        <div className="grid grid-cols-1 lg:grid-cols-12 gap-6 no-print">
          <div className="lg:col-span-8 bg-slate-900/40 p-6 rounded-[2.5rem] border border-white/5 backdrop-blur-xl">
             <div className="flex justify-between items-center mb-6">
                <h3 className="text-[10px] font-bold text-indigo-400 uppercase tracking-widest flex items-center gap-2"><Layout size={12} /> Matrix Configuration</h3>
                <div className="flex bg-black/40 p-1 rounded-xl border border-white/5">
                  <button onClick={() => setProfile({...profile, gender: 'Male'})} className={`px-4 py-1.5 rounded-lg text-[10px] font-black transition-all ${profile.gender === 'Male' ? 'bg-indigo-600 text-white shadow-lg' : 'text-slate-600'}`}>MALE</button>
                  <button onClick={() => setProfile({...profile, gender: 'Female'})} className={`px-4 py-1.5 rounded-lg text-[10px] font-black transition-all ${profile.gender === 'Female' ? 'bg-rose-600 text-white shadow-lg' : 'text-slate-600'}`}>FEMALE</button>
                </div>
             </div>
             <div className="grid grid-cols-3 gap-3 mb-6">
                {['birthYear', 'birthMonth', 'birthDay'].map((key, i) => (
                  <div key={key} className="space-y-1">
                    <span className="text-[9px] text-slate-500 font-bold uppercase ml-1">{['Year', 'Month', 'Day'][i]}</span>
                    <select value={profile[key]} onChange={(e) => setProfile({...profile, [key]: parseInt(e.target.value)})} className="w-full bg-slate-950 border border-white/10 rounded-xl p-3 text-sm font-black focus:border-indigo-500 outline-none">
                      {[birthYears, months, days][i].map(o => <option key={o} value={o}>{o}</option>)}
                    </select>
                  </div>
                ))}
             </div>
             <div className="pt-4 border-t border-white/5">
                <span className="text-[9px] text-emerald-500 font-bold uppercase tracking-widest mb-4 block">Analysis Flow Target</span>
                <div className="flex gap-2 overflow-x-auto no-scrollbar pb-1">
                  {flowYears.map(y => (
                    <button key={y} onClick={() => setProfile({...profile, targetYear: y})} className={`shrink-0 px-5 py-2.5 rounded-xl text-xs font-black transition-all border ${profile.targetYear === y ? 'bg-emerald-600 border-emerald-400 text-white' : 'bg-slate-950 border-white/5 text-slate-500'}`}>{y}</button>
                  ))}
                </div>
             </div>
          </div>

          <div className="lg:col-span-4 bg-slate-900/20 p-6 rounded-[2.5rem] border border-white/5 flex flex-col justify-center items-center text-center">
            <h3 className="text-[10px] font-bold text-slate-500 uppercase tracking-widest mb-4">Flow Indicator</h3>
            <div className="text-6xl font-black text-emerald-400 tracking-tighter mb-2">{results.personalYear}</div>
            <p className="text-[9px] text-slate-500 uppercase font-black px-4">
              {results.personalYear === 4 ? "Year of Systemization" : "Year of Fluctuating Opportunity"}
            </p>
          </div>
        </div>

        {/* 报告主体内容 */}
        <div id="report-content" className="grid grid-cols-1 lg:grid-cols-3 gap-6 items-stretch">
          
          <div className="flex flex-col gap-6">
            <div className="bg-slate-900/60 p-6 rounded-[2.5rem] border border-white/10 shadow-2xl print:bg-white print:border-slate-300 print:text-slate-900">
              <div className="flex items-center gap-4 mb-6 pb-6 border-b border-white/5 print:border-slate-200">
                <div className={`w-14 h-14 rounded-2xl ${profile.gender === 'Male' ? 'bg-blue-600/10' : 'bg-rose-600/10'} flex items-center justify-center border border-white/5 print:bg-slate-50`}>
                  {profile.gender === 'Male' ? <Mars className="text-blue-400 print:text-blue-700" size={24}/> : <Venus className="text-rose-400 print:text-rose-700" size={24}/>}
                </div>
                <div className="flex-1">
                   {isEditingName ? <input type="text" value={profile.name} onChange={(e) => setProfile({...profile, name: e.target.value})} onBlur={() => setIsEditingName(false)} className="bg-black/50 border border-indigo-500/30 rounded-lg px-2 py-1 text-xl font-black text-white w-full" autoFocus /> : <h2 className="text-2xl font-black tracking-tight print:text-slate-950">{profile.name}</h2>}
                   <p className="text-[10px] text-slate-500 uppercase font-mono mt-1">ID: {profile.birthYear}{profile.birthMonth}{profile.birthDay}</p>
                </div>
              </div>
              <div className="space-y-4">
                <div className="flex justify-between items-center p-4 bg-black/40 rounded-2xl border border-white/5 print:bg-slate-50 print:border-slate-200">
                   <span className="text-[9px] text-slate-500 uppercase font-black">Main Apex</span>
                   <div className="flex items-center gap-2">
                      <span className={`text-xl font-black ${numMap[results.F]?.text}`}>{results.F}</span>
                      <span className="text-[10px] font-bold text-slate-400 uppercase">{numMap[results.F]?.name}</span>
                   </div>
                </div>
                <div className="flex justify-between items-center p-4 bg-black/40 rounded-2xl border border-white/5 print:bg-slate-50 print:border-slate-200">
                   <span className="text-[9px] text-slate-500 uppercase font-black">Sitting Root</span>
                   <div className="flex items-center gap-2">
                      <span className="text-xl font-black text-rose-500">{results.K}</span>
                      <span className="text-[10px] font-bold text-slate-400 uppercase">核心</span>
                   </div>
                </div>
              </div>
            </div>

            <div className="bg-slate-900/40 p-6 rounded-[2.5rem] border border-white/5 print:bg-white print:border-slate-300">
              <h3 className="text-[10px] font-bold text-slate-500 uppercase tracking-widest mb-4 flex items-center gap-2"><Hash size={12}/> Calculation Equations</h3>
              <div className="space-y-2">
                 {results.steps.map(step => (
                   <div key={step.id} className={`flex justify-between items-center p-3 rounded-xl border ${step.highlight ? 'bg-indigo-600/10 border-indigo-500/20' : 'bg-black/20 border-white/5'} print:border-slate-200`}>
                      <div className="flex flex-col">
                         <span className="text-[9px] text-slate-400 font-bold uppercase">{step.label}</span>
                         <span className="text-[8px] text-slate-500 font-mono italic">{step.formula}</span>
                      </div>
                      <span className={`text-sm font-black ${step.highlight ? 'text-indigo-400 print:text-indigo-700' : 'text-slate-300 print:text-slate-900'}`}>{step.val}</span>
                   </div>
                 ))}
              </div>
            </div>
          </div>

          <div className="lg:col-span-2 bg-slate-950 p-10 rounded-[3rem] border border-white/10 flex flex-col items-center justify-center relative print:bg-white print:border-slate-300 print:text-slate-950">
            <div className="relative w-80 h-80 py-4">
              <svg className="absolute inset-0 w-full h-full overflow-visible opacity-20 print:opacity-70" viewBox="0 0 100 100">
                <polygon points="50,5 95,85 5,85" fill="none" stroke={profile.gender === 'Male' ? '#3b82f6' : '#ec4899'} strokeWidth="1" />
                <line x1="50" y1="5" x2="50" y2="85" stroke="rgba(99,102,241,0.3)" strokeWidth="0.4" strokeDasharray="1 1" />
              </svg>

              <div className="absolute top-0 left-1/2 -translate-x-1/2 -translate-y-1/2 flex flex-col items-center">
                 <div className={`w-20 h-20 rounded-[2rem] bg-gradient-to-br ${numMap[results.F]?.color} flex items-center justify-center text-white text-4xl font-black shadow-2xl rotate-45 border-4 border-slate-950 print:bg-white print:border-slate-900 print:text-slate-950 print:rotate-0 print:border-2`}>
                   <span className="print:rotate-0 -rotate-45">{results.F}</span>
                 </div>
                 <span className="text-[9px] text-indigo-400 font-black uppercase mt-12 tracking-[0.4em]">Personality Apex</span>
              </div>

              <div className="absolute top-[45%] left-0 -translate-x-1/2"><div className="w-12 h-12 bg-slate-900 border-2 border-indigo-500/30 rounded-2xl flex items-center justify-center font-black text-indigo-300 print:bg-slate-50 print:border-slate-300 print:text-slate-900">{results.D}</div></div>
              <div className="absolute top-[45%] right-0 translate-x-1/2"><div className="w-12 h-12 bg-slate-900 border-2 border-indigo-500/30 rounded-2xl flex items-center justify-center font-black text-indigo-300 print:bg-slate-50 print:border-slate-300 print:text-slate-900">{results.E}</div></div>

              <div className="absolute bottom-0 left-0 -translate-x-1/2 translate-y-1/2 flex flex-col items-center">
                 <div className="w-10 h-10 bg-slate-900 border border-white/5 rounded-xl flex items-center justify-center font-black text-slate-500 print:bg-slate-100 print:border-slate-200">{results.A}</div>
                 <span className="text-[7px] text-slate-600 mt-1 font-bold tracking-widest">Base-A</span>
              </div>
              <div className="absolute bottom-0 left-1/2 -translate-x-1/2 translate-y-1/2 flex flex-col items-center">
                 <div className="w-10 h-10 bg-slate-900 border border-white/5 rounded-xl flex items-center justify-center font-black text-slate-500 print:bg-slate-100 print:border-slate-200">{results.B}</div>
                 <span className="text-[7px] text-slate-600 mt-1 font-bold tracking-widest">Core-B</span>
              </div>
              <div className="absolute bottom-0 right-0 translate-x-1/2 translate-y-1/2 flex flex-col items-center">
                 <div className="w-10 h-10 bg-slate-900 border border-white/5 rounded-xl flex items-center justify-center font-black text-slate-500 print:bg-slate-100 print:border-slate-200">{results.C}</div>
                 <span className="text-[7px] text-slate-600 mt-1 font-bold tracking-widest">Base-C</span>
              </div>

              <div className="absolute bottom-[-20%] left-1/2 -translate-x-1/2 flex flex-col items-center">
                 <div className="w-16 h-16 bg-slate-900 border-4 border-rose-500/30 rounded-full flex items-center justify-center text-rose-500 text-2xl font-black animate-pulse print:animate-none print:bg-white print:border-slate-950 print:text-slate-950">
                    {results.K}
                 </div>
                 <span className="text-[8px] text-rose-500 font-black uppercase mt-2 tracking-widest print:text-rose-700">Root Sitting</span>
              </div>
            </div>

            <div className="mt-32 w-full grid grid-cols-2 gap-8 border-t border-white/10 pt-8 print:border-slate-200">
               <div>
                 <h4 className="text-[10px] font-bold text-indigo-400 uppercase mb-2">人格矩阵解析</h4>
                 <p className="text-[11px] text-slate-400 leading-relaxed print:text-slate-700 italic">
                   主命数 {results.F} 号人：爆发力极强。思维跳跃，善于破局。在 2026 架构年，您的核心课题是“建立秩序以容纳创意”。
                 </p>
               </div>
               <div>
                 <h4 className="text-[10px] font-bold text-emerald-400 uppercase mb-2">流年战略重心</h4>
                 <div className="flex items-center gap-4">
                    <span className="text-4xl font-black text-emerald-400">{results.personalYear}</span>
                    <p className="text-[10px] text-slate-500 uppercase leading-snug font-bold">
                      {results.personalYear === 4 ? "【架构之年】重点：严控法务合同，理顺财务流向，建立青训标准化流程，稳扎稳打。" : "周期性能量调整中。"}
                    </p>
                 </div>
               </div>
            </div>
          </div>
        </div>

        {/* AI 分析报告区域 */}
        <div className="flex flex-col gap-6">
           <div className="flex justify-between items-center no-print">
              <h3 className="text-[10px] font-bold text-slate-500 uppercase tracking-[0.3em] flex items-center gap-2"><Sparkles size={14} className="text-indigo-400"/> AI Strategic Deep Insight</h3>
              <button 
                onClick={handleAiAnalyze}
                disabled={aiLoading}
                className="px-6 py-3 bg-indigo-600 hover:bg-indigo-500 text-white rounded-xl text-[10px] font-black uppercase tracking-widest flex items-center gap-2 shadow-lg shadow-indigo-600/30 transition-all active:scale-95"
              >
                {aiLoading ? <Loader2 className="animate-spin" size={14}/> : <Sparkles size={14}/>} 生成/刷新分析报告
              </button>
           </div>

           {aiResponse ? (
             <div className="bg-slate-900/60 p-10 rounded-[3rem] border border-white/10 shadow-2xl relative overflow-hidden print:bg-white print:border-slate-300 print:text-slate-950 print:shadow-none">
                <div className="flex items-center gap-3 mb-8 text-indigo-400 print:text-indigo-700">
                  <FileText size={24} />
                  <h3 className="text-base font-black uppercase tracking-[0.2em]">战略顾问 波 (Bo) 的全相位决策蓝图</h3>
                </div>
                <div className="text-[14px] text-slate-300 leading-[1.8] border-l-4 border-indigo-500/20 pl-8 print:text-slate-800 print:border-indigo-700 print:pl-6 print:not-italic">
                   {aiResponse.split('\n').map((para, i) => (
                     <p key={i} className="mb-4">{para}</p>
                   ))}
                </div>
                <div className="mt-10 pt-6 border-t border-white/5 text-[9px] text-slate-600 font-mono flex justify-between no-print">
                   <span className="uppercase tracking-widest">AUTHENTICATED STRATEGIC DOCUMENT</span>
                   <span>GEN-TIME: {new Date().toLocaleTimeString()}</span>
                </div>
             </div>
           ) : (
             <div className="bg-slate-900/20 border-2 border-dashed border-white/5 rounded-[3rem] p-20 text-center no-print opacity-40">
                <MessageSquare size={48} className="mx-auto text-slate-800 mb-4" />
                <p className="text-[11px] text-slate-600 uppercase font-black tracking-[0.2em] italic">Waiting for Command to Generate Strategy Report...</p>
             </div>
           )}
        </div>

        {/* Footer */}
        <div className="text-center pb-8 opacity-20 print:border-t print:pt-8 print:mt-12 print:opacity-100 print:text-slate-400">
          <p className="text-[9px] uppercase tracking-[0.6em] font-mono">Bo Intelligence Matrix OS • Strategic Analytics • Precision Logic</p>
        </div>
      </div>
      
      <style>{`
        @media print {
          body { background-color: white !important; color: black !important; padding: 0 !important; margin: 0 !important; -webkit-print-color-adjust: exact; }
          .no-print { display: none !important; }
          .only-print { display: block !important; }
          .min-h-screen { min-height: auto !important; height: auto !important; background: white !important; padding: 0 !important; }
          .max-w-5xl { max-width: 100% !important; width: 100% !important; margin: 0 !important; padding: 25px !important; }
          text-white { color: black !important; }
          #report-content { display: grid !important; }
          svg line, svg polygon { stroke: #000 !important; opacity: 0.5 !important; }
          page-break-inside: avoid;
        }
        .only-print { display: none; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
        .custom-scrollbar::-webkit-scrollbar { width: 3px; }
        .custom-scrollbar::-webkit-scrollbar-track { background: transparent; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: rgba(99, 102, 241, 0.2); border-radius: 10px; }
      `}</style>
    </div>
  );
};

export default App;
