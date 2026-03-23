<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>行车记录仪 - VOC 智能分析与客服中台</title>
    <script src="https://cdn.sheetjs.com/xlsx-0.20.1/package/dist/xlsx.full.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f4f7f6; margin: 0; padding: 20px; color: #333; }
        .header { text-align: center; margin-bottom: 20px; }
        .header h1 { color: #2c3e50; margin-bottom: 5px;}
        .container { display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; }
        .card { background: white; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); padding: 20px; width: calc(50% - 30px); min-width: 400px; box-sizing: border-box; }
        .full-width { width: 100%; }
        .section { background: #fff; padding: 20px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); margin-bottom: 20px; display: flex; gap: 15px; align-items: center; justify-content: center; flex-wrap: wrap;}
        .import-section { background: #e8f8f5; border: 2px dashed #1abc9c; flex-direction: column; }
        .email-section { background: #ebf5fb; border: 2px solid #3498db; flex-direction: column; align-items: flex-start;}
        .address-section { background: #fef9e7; border: 2px solid #f1c40f; flex-direction: column; align-items: flex-start;}
        input, select, button { padding: 8px; border: 1px solid #ccc; border-radius: 4px; font-size: 14px; box-sizing: border-box;}
        button { background-color: #3498db; color: white; border: none; cursor: pointer; transition: 0.3s; font-weight: bold; padding: 10px 15px;}
        button:hover { background-color: #2980b9; }
        .export-btn { background-color: #27ae60; margin-top: 15px; width: auto; }
        .action-btn { background-color: #e67e22; font-size: 16px; padding: 10px 20px; margin-left: 10px;}
        textarea { width: 100%; padding: 10px; border: 1px solid #bdc3c7; border-radius: 4px; font-size: 14px; margin-top: 10px; font-family: Arial, sans-serif; box-sizing: border-box;}
        canvas { max-width: 100%; background-color: white; }
        
        /* 情绪雷达与地址解析专属样式 */
        .sentiment-
