<!DOCTYPE html>
<html>
<head>
    <title>Data Input Page</title>
    <link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<style>
        body {
            font-family: Arial, sans-serif;
        }
        h2 {
            color: #333;
        }
        form {
            background-color: #f9f9f9;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 5px;
            box-shadow: 0px 0px 10px #ccc;
        }
        .form-group {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }
        .form-group label {
            margin-right: 10px;
        }
        input[type="text"], select {
            padding: 5px;
            width: 200px;
        }
        input[type="submit"] {
            margin-top: 10px;
            padding: 5px 20px;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #0056b3;
        }
        #displayData {
            white-space: pre-wrap;
            word-wrap: break-word;
        }

        .form-group {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1em;
        }
        label {
            flex: 1;
        }
        input {
            flex: 2;
        }

        .form-group {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .form-group label, .form-group input[type="text"], .form-group select {
            margin-right: 10px;
        }

        .form-group div {
            display: flex;
            align-items: center;
        }
    </style>
    <!-- The rest of your head content -->

</head>
<body>
    <!-- The content of your first page -->
    <h2>Data Input Form</h2>

    <form id="dataForm">
        <div id="sortable">
            <div class="form-group">
                <label for="torqueCurve">扭力曲线图(torqueCurve):</label>
                <input type="text" id="torqueCurve" name="torqueCurve" data-chinese-name="扭力曲线图" disabled>
                <div>
                    <input type="checkbox" id="include_torqueCurve" onchange="toggleInput('include_torqueCurve')">
                    <label for="include_torqueCurve">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="screwThread">螺丝是否有入牙(screwThread):</label>
                <select id="screwThread" name="screwThread" data-chinese-name="螺丝是否入牙" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_screwThread" onchange="toggleInput('include_screwThread')">
                    <label for="include_screwThread">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="electricBatch">电批反拧后复锁(electricBatch):</label>
                <select id="electricBatch" name="electricBatch" data-chinese-name="电批反拧后复锁" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_electricBatch" onchange="toggleInput('include_electricBatch')">
                    <label for="include_electricBatch">Include</label>
                </div>

            </div>

            <div class="form-group">
                <label for="screwAngle">本次检查角度(screwAngle):</label>
                <input type="text" id="screwAngle" name="screwAngle" data-chinese-name="本次检查角度" disabled>
                <div>
                    <input type="checkbox" id="include_screwAngle" onchange="toggleInput('include_screwAngle')">
                    <label for="include_screwAngle">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="torque">本次检查扭矩(torque):</label>
                <input type="text" id="torque" name="torque" data-chinese-name="本次检查扭矩" disabled>
                <div>
                    <input type="checkbox" id="include_torque" onchange="toggleInput('include_torque')">
                    <label for="include_torque">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="screwMisalign">侧相机螺丝图像螺丝是否取歪(screwMisalign):</label>
                <select id="screwMisalign" name="screwMisalign" data-chinese-name="侧相机螺丝图像螺丝是否取歪" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_screwMisalign" onchange="toggleInput('include_screwMisalign')">
                    <label for="include_screwMisalign">Include</label>
                </div>
            </div>
            
            <div class="form-group">
                <label for="sleeveSwinging">批头侧相机图片批头套筒是否明显摆动(sleeveSwinging):</label>
                <select id="sleeveSwinging" name="sleeveSwinging" data-chinese-name="批头侧相机图片批头套筒是否明显摆动" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_sleeveSwinging" onchange="toggleInput('include_sleeveSwinging')">
                    <label for="include_sleeveSwinging">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="nutExceeds">螺帽是否超出套筒下边(nutExceeds):</label>
                <select id="nutExceeds" name="nutExceeds" data-chinese-name="螺帽是否超出套筒下边" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_nutExceeds" onchange="toggleInput('include_nutExceeds')">
                    <label for="include_nutExceeds">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="screwMatch">螺丝与套筒是否匹配(screwMatch):</label>
                <select id="screwMatch" name="screwMatch" data-chinese-name="螺丝与套筒是否匹配" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_screwMatch" onchange="toggleInput('include_screwMatch')">
                    <label for="include_screwMatch">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="assemblyAbnormality">检查组装纠偏图像是否有异常(assemblyAbnormality ):</label>
                <select id="assemblyAbnormality" name="assemblyAbnormality" data-chinese-name="检查组装纠偏图像是否有异常" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_assemblyAbnormality" onchange="toggleInput('include_assemblyAbnormality')">
                    <label for="include_assemblyAbnormality">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="BGRecasting">拆完螺丝后BG复投OK(BGRecasting):</label>
                <select id="BGRecasting" name="BGRecasting" data-chinese-name="拆完螺丝后BG复投OK" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_BGRecasting" onchange="toggleInput('include_BGRecasting')">
                    <label for="include_BGRecasting">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="angleMatch">检查电批取螺丝角度范围是否符合90°±3°(angleMatch):</label>
                <select id="angleMatch" name="angleMatch" data-chinese-name="检查电批取螺丝角度范围是否符合90°±3°" disabled>
                    <option value="是">是</option>
                    <option value="否">否</option>
                </select>
                <div>
                    <input type="checkbox" id="include_angleMatch" onchange="toggleInput('include_angleMatch')">
                    <label for="include_angleMatch">Include</label>
                </div>
            </div>

            <div class="form-group">
                <label for="vacuumMatch">电批1真空值是否大于等于75(vacuumMatch):</label>
                <input type="text" id="vacuumMatch" name="vacuumMatch" data-chinese-name="电批1真空值是否大于等于75" disabled>
                <div>
                    <input type="checkbox" id="include_vacuumMatch" onchange="toggleInput('include_vacuumMatch')">
                    <label for="include_vacuumMatch">Include</label>
                </div>
            </div>

            <input type="submit" value="Submit">
        </div>
    </form>
    <label for="outputFormat">Output Format:</label>
    <select id="outputFormat">
        <option value="both">Both English and Chinese</option>
        <option value="english">Only English</option>
        <option value="chinese">Only Chinese</option>
    </select>

    <h2>Your Input:</h2>
    <pre id="displayData"></pre>

    <button id="sendButton">Send</button><br>
    <textarea id="response" rows="8" cols="150" readonly placeholder="Response will appear here..."></textarea>

    <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
    <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>

    <!-- The rest of your scripts -->
    <script>
        // Toggle input
        function toggleInput(checkboxId) {
            var checkbox = document.getElementById(checkboxId);
            var inputId = checkboxId.replace('include_', '');
            var input = document.getElementById(inputId);
            input.disabled = !checkbox.checked;
        }

        // Set initial state of inputs
        window.onload = function() {
            var checkboxes = ['include_torqueCurve', 'include_screwThread', 'include_electricBatch', 'include_screwAngle', 'include_torque', 'include_screwMisalign', 'include_sleeveSwinging', 'include_nutExceeds', 'include_assemblyAbnormality', 'include_BGRecasting', 'include_angleMatch', 'include_vacuumMatch'];
            checkboxes.forEach(function(checkboxId) {
                toggleInput(checkboxId);
            });
        };

        var dataForm = document.getElementById('dataForm');
        var outputFormat = document.getElementById('outputFormat');
        var displayData = document.getElementById('displayData');

        var englishData = {};
        var chineseData = {};
        var bothData = {};

        function displaySelectedFormat() {
            var selectedFormat = outputFormat.value;
            var displayDataObject;

            switch (selectedFormat) {
                case "english":
                    displayDataObject = englishData;
                    break;
                case "chinese":
                    displayDataObject = chineseData;
                    break;
                case "both":
                    displayDataObject = bothData;
                    break;
            }

            displayData.textContent = JSON.stringify(displayDataObject, null, 2);
        }

        dataForm.addEventListener('submit', function (e) {
            e.preventDefault();

            for (var i = 0; i < dataForm.elements.length; i++) {
                var element = dataForm.elements[i];

                if (element.name && document.getElementById('include_' + element.name).checked) {
                    englishData[element.name] = element.value;
                    var chineseName = element.getAttribute('data-chinese-name');
                    chineseData[chineseName] = element.value;
                    var keyName = chineseName ? (chineseName + element.name) : element.name;
                    bothData[keyName] = element.value;
                }
            }

            displaySelectedFormat();
        });

        outputFormat.addEventListener('change', displaySelectedFormat);

        // Initialize sortable
        $("#sortable").sortable();
        $("#sortable").disableSelection();

        const sendButton = document.getElementById('sendButton')
        const responseTextarea = document.getElementById('response');
        const sessionStartText = 'Please start a session first.';

        document.getElementById('sendButton').addEventListener('click', async () => {



<!--            for (var i = 0; i < dataForm.elements.length; i++) {-->
<!--                var element = dataForm.elements[i];-->

<!--                if (element.name && document.getElementById('include_' + element.name).checked) {-->
<!--                    englishData[element.name] = element.value;-->
<!--                    var chineseName = element.getAttribute('data-chinese-name');-->
<!--                    chineseData[chineseName] = element.value;-->
<!--                    var keyName = chineseName ? (chineseName + element.name) : element.name;-->
<!--                    bothData[keyName] = element.value;-->
<!--                }-->
<!--            }-->
<!--            console.log("prompt", prompt);-->
<!--            const prompt = chineseName;-->

            const prompt = JSON.stringify(bothData, null, 2);
            console.log("prompt", prompt);
            const response = await fetch('http://127.0.0.1:8000/chat', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    prompt: prompt,
                })
            });

            const jsonResponse = await response.json();
            console.log("jsonResponse", jsonResponse);
            document.getElementById('response').value = jsonResponse.response;

        });
    </script>

</body>
</html>
