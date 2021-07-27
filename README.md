# Create-ppt-using-javascript using PPTXGEN API

# include inside header tag
<script src="pptxgen.bundle.js"></script>

inside script
#first add
let pptx = new PptxGenJS();


#To create slide with background image , header

let slide = pptx.addSlide();
// let slide = pptx.addSlide("MASTER_NAME");
// slide = pptx.addSlide("TITLE_SLIDE");
// 3. Add one or more objects (Tables, Shapes, Images, Text and Media) to the Slide
slide.background = { path: "bg1.jpg" }; // image: url
slide.addText("COMPLAINT ANALYSIS REPORT", {
    x: 0,
    y: "20%",
    w: "100%", 
    h: 0.55,
    fontSize: 20,
    bold:true,
    underline:true,
    color: "363636",
    align: pptx.AlignH.center,
});


#To create slide with chart line,bar , header use below code

slide3.addChart(pptx.ChartType.line, dataChartAreaLine3, { x: 0.3, y: 0.8, w: "46%", h: 2 });

let dataChartAreaLine31 = [
    {
        labels: [],
        values: [],
    },
    {
        labels: ["18:16", "18:17", "18:19", "18:21", "18", "18:27", "18:28", "18:30", "18:32", "18:34", "18:36", "18:38"],
        values: [120, -25, -30, -29, -31, -29, -30, -29, -29, -31, -31, -30],
    },
    
];

slide3.addChart(pptx.ChartType.line, dataChartAreaLine31, { x: 5, y: 0.8, w: "48%", h: 2,});
