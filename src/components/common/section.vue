<template>
    <div >
      <div class="main margin" id="Business">
          <div class="ind_box1">
              <p class="ind_bt">Business</p>
              <p class="ind_btcha">业务领域</p>          
            <div class="col-flex" >
              
                <template v-for=" (temp ,index) in business">
                    <div :key="temp.title" style="position:relative;width:230px">
                        <transition  name="slide-fade">
                            <a href="javascript:void(0)" class="x1"  v-if="temp.show" @click="sho(temp.show,index)">
                        			  <div class="x1_ico" :class="temp.class"></div>
                        			  <p class="x1_bt">{{temp.title}}</p>
                        			  <p class="x1_bteng">{{temp.detail}}</p>
                            </a>
                        </transition>
                        <transition  name="slide-fade">
                           
                        			  <p class="x1 pp"  v-if="!temp.show" @click="sho(temp.show,index)">{{temp.p}}</p>
                  
                        </transition>     
                          </div>         
                </template>
        

            </div>
          </div>
      </div>
      <div class="ind_box2" id="AboutUs">
      		<p class="ind_bt">AboutUs</p>
      		<p class="ind_btcha">关于我们</p>
      		<div class="ind_x2">
           	<img class="x2_img" width="490" height="355" src="../../assets/img/img3.jpg" >
      			<p class="x2_bt">关于中安</p>
      			<div class="x2_sm">
      				<p>
      	        中安融资租赁股份有限公司 
      	        简   介 
      	        中安融资租赁股份有限公司成立于江苏，是经国家商务部批准成立的中外合资融资租赁公司，其业务受理范围是面向全国的融资租赁业务，专注中国中小企业。基于客户类别的划分，对特定客户提供全面的金融服务。</p>
      			</div>
      		</div>
      </div>  
      <!-- <div class="main margin ind_box3" >
      		<p class="ind_bt">News</p>
      		<p class="ind_btcha">公司新闻</p>
      		<div class="k1 ind_x3">
      			<div class="l left">
      				<img  src="../../assets/img/img4.jpg" width="360" height="250" alt="">
                      <a href="NewsInfo.aspx?id=53">
      				<p class="left_bt">嘉德租赁与一汽解放签5亿合作协议</p>
      				<p class="left_sm">
      	       6月23日，嘉德国际融资租赁股份有限公司与一汽解放汽车销售有限公司战略...</p>
                          </a>
      			</div>
      			<ul class="r right">
      				<li><a href="NewsInfo.aspx?id=40">
      					<span class="num l">01</span>
      					<div class="r wz">
      						<p class="x3_bt l">嘉德租赁与上汽红岩签5亿合同</p>
      						<p class="x3_time r">2016-08-15</p>
      						<p class="x3_sm clear">
      	          日前，嘉德国际融资租赁有限公司与上汽依维柯红岩商用车有限公司在大连签订合作协议，根据协议，嘉德租赁为上汽红岩的终端用户提供5亿元的授...</p>
      					</div>
      				</a></li>
      				<li><a href="NewsInfo.aspx?id=39">
      					<span class="num l">02</span>
      					<div class="r wz">
      						<p class="x3_bt l">嘉德租赁完成股份制改造</p>
      						<p class="x3_time r">2016-03-03</p>
      						<p class="x3_sm clear">
                  
                  
                  
      	       2016年3月1日，嘉德国际融资租赁有限公司顺利完成股份制改造，这标志着嘉德租赁登录资本市场迈出了关键一步。 


      	       ...</p>
      					</div>
      				</a></li>

      				<li><a href="NewsInfo.aspx?id=38">
      					<span class="num l">03</span>
      					<div class="r wz">
      						<p class="x3_bt l">嘉德租赁获准接入央行企业征信查询系统</p>
      						<p class="x3_time r">2015-08-11</p>
      						<p class="x3_sm clear">
                  	依中国人民银行征信中心中征便函242号文件通知，嘉德国际融资租赁有限公司成为本批次获准接入中国人民银行征信系统18家机构之一。接入央行企业征信...</p>
      					</div>
      				</a></li>

      			</ul>
      		</div>
      </div>   -->
      <div class="hyzx" id="IndustryNews">
        <div class="main margin ind_box4">
            <p class="ind_bt">IndustryNews</p>
            <p class="ind_btcha">行业资讯</p>  
            <div>
            <ul class="new2">
              <li v-for="(temp,index) in new2" :key="temp.src" @click="showIndex(index+1)">
                <a href="javascript:void(0)">
	        	  	<img class="li_img" :src="temp.src" width="240" height="150" alt="" >
	        	  	<div class="wz">
	        	  	<p class="bt">{{temp.title}}</p>
	        	  	<p class="sm">
                  {{temp.detail}}
	               </p>
	        	  	<p class="time right">{{temp.time}}</p>
	        	  	<div class="clear"></div>
	        	  	<p class="more">查看详细 &gt;&gt;</p>
	        	  	</div>
	        	  </a>
              </li>
	          </ul>           
            </div>
        </div>  
      </div>
      <div class="hyzx flfg" id="LawsRegulations">
        <div class="main margin ind_box4">
            <p class="ind_bt">LawsRegulations</p>
            <p class="ind_btcha">法律法规</p>  
            <div>
            <ul class="new2">
              <li v-for="(temp,index) in new3" :key="temp.src" @click="showIndex(index+4)">
                <a href="javascript:void(0)">
	        	  	<img class="li_img" :src="temp.src" width="240" height="150" alt="" >
	        	  	<div class="wz">
	        	  	<p class="bt">{{temp.title}}</p>
	        	  	<p class="sm">
                  {{temp.detail}}
	               </p>
	        	  	<p class="time right">{{temp.time}}</p>
	        	  	<div class="clear"></div>
	        	  	<p class="more">查看详细 &gt;&gt;</p>
	        	  	</div>
	        	  </a>
              </li>
	          </ul>           
            </div>
        </div>  
      </div> 
      <div class="hyzx join" id="JoinUs">
        <div class="main margin ind_box4">
            <p class="ind_bt">JoinUs</p>
            <p class="ind_btcha">加入我们</p>            
            <ul class="bod">
            	<li>
            		<p class="bt">
            			核心价值观
            		</p>
            		<div class="sm">
            			<p class="sm_p">
            				团结 进取 创新 发展
            			</p>
            		</div>
            	</li>
            	<li>
            		<p class="bt">
            			公司愿景
            		</p>
            		<div class="sm">
            			<p class="sm_p">
            				成为国内一流、具有国际影响力的专业租赁公司
            			</p>
            		</div>
            	</li>
            	<li>
            		<p class="bt">
            			公司使命
            		</p>
            		<div class="sm">
            			<p class="sm_p">
            				为客户提供全方位、高效率、低成本的融资租赁解决方案，凭借专业的服务团队以专业的视角不断为客户创新方案。架起产业资本与金融资本间的桥梁，在租赁专业领域实现公司价值成长，为客户创造价值，为员工创造施展才华的平台，为社会创造财富。
            			</p>
            		</div>
            	</li>
            	<li>
            		<p class="bt">
            			公司战略
            		</p>
            		<div class="sm">
            			<p class="sm_p">
            				设计一流产品 提供一流服务&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 设一流公司<br>
            塑造专业、高效的一流品牌&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;创造一流业绩<br>
            打造规范、文件的一流企业&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;实现一流管理<br>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 组建一流团队<br>
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 争当一流员工
            			</p>
            		</div>
            	</li>
            </ul>          
        </div>  
      </div>  
      <div class="margin" style="width:1100px;height:700px;margin-top:115px" id="ContactWay">
            <p class="ind_bt">ContactWay </p>
            <p class="ind_btcha">联系地址</p>          
          <v-map></v-map>
      </div>
      <el-row id="el">

      
      <el-dialog
        title="提示"
        :visible.sync="dialogVisible"
        width="80%"
        >
        <div v-if="index ==1" class="new_inner">
	        <h1 class="news_h1">汽车融资租赁中的风险点及其应对措施</h1>
	        <h3 class="news_h3">发布时间：2017-08-03</h3>
	        <div class="newp">
          <p class="MsoNormal" style="text-indent:18.0pt;">
          	引导语：汽车融资租赁，是指融资租赁公司根据承租人对租赁车辆与供应商的选择，与供应商签订《车辆买卖合同》购买相应车辆并根据其与承租人签订的《融资租赁合同》出租给承租人使用，承租人分期向融资租赁公司支付租金，租赁期满，租金付讫后，出租人将租赁车辆以象征性的价格无条件过户给承租人的交易行为。以下是相关的风险点及其应对措施资料，欢迎大家阅读学习。
          </p>
          <p class="MsoNormal">
          	<strong> </strong><strong>(</strong><strong>一</strong><strong>)</strong><strong>遭遇合同诈骗的风险</strong>
          </p>
          <p class="MsoNormal">
          	汽车融资租赁业务的蓬勃发展以及汽车融资租赁公司普遍风控意识不强，给一些不法分子甚至单位铤而走险提供了可乘之机，利用融资租赁业务的特殊性对汽车融资租赁公司实施合同诈骗。
          </p>
          <p class="MsoNormal">
          	应对措施：
          </p>
          <p class="MsoNormal">
          	1、对承租人及担保财产、担保人进行充分的尽职调查、分析及核实，除常规的资料信息外，主要关注点还应包括：承租人及担保人的工作单位及工作稳定性、薪酬、单位职务及社会职务、家庭成员情况及其财力、购买的车辆是否与本人实际情况匹配、承租人及担保人的征信情况、涉诉情况、被行政处罚情况等。
          </p>
          <p class="MsoNormal">
          	2、在相关合同条文中明确约定或者单独出具声明，汽车融资租赁公司将在发现合同诈骗情形时第一时间向公安机关报案，其所提交的所有材料将作为证据使用，这一点对于惯犯不一定能起到很好的效果，但在一定程度上也能起到震慑作用;
          </p>
          <p class="MsoNormal">
          	3、保留好相应尽职调查原始资料，在发现合同诈骗时，尽快整理报案材料并向公安机关报案，在报案的环节上，除了准备详尽资料外，最好能通过较短的篇幅或者图形可视化的模式向公安机关描述整个合同诈骗的过程，以降低公安机关对事实的认定不清而将案件归为民事经济纠纷而拒绝立案的风险。
          </p>
          <p class="MsoNormal">
          	<strong> </strong><strong>(</strong><strong>二</strong><strong>)</strong><strong>租金拖欠的风险</strong>
          </p>
          <p class="MsoNormal">
          	租金拖欠风险是汽车融资租赁业务中最常见的风险，主要是指承租人到期不能按时或者足额向汽车融资租赁公司交纳租金的行为。
          </p>
          <p class="MsoNormal">
          	应对措施：发生租金拖欠，承租人给出的理由往往真真假假，汽车融资租赁公司不能以承租人所描述的理由作为其后续应对措施的依据，建议汽车融资租赁公司以拖欠时间为依据，将拖欠租金行为的对应措施划分三类：
          </p>
          <p class="MsoNormal">
          	1、关注，此时公司业务人员应对承租人进行催收并调查拖欠原因;
          </p>
          <p class="MsoNormal">
          	2、严重关注，由公司法务部门或者律师起草相关函件以公司名义向承租人发出，并告知其法律后果;
          </p>
          <p class="MsoNormal">
          	3、司法措施，提起诉讼或者仲裁。
          </p>
          <p class="MsoNormal">
          	除此之外，为避免进一步的损失，承租人在收到汽车融资租赁公司发出的函件后仍拖欠租金的，建议承租人在安全得到保证的情况下组织力量实施自力救济，或者在承租人签署具有强制执行效力的融资租赁合同并进行公证的前提下申请法院强制执行。
          </p>
          <p class="MsoNormal">
          	<strong> </strong><strong>(</strong><strong>三</strong><strong>)</strong><strong>保证金、违约金认定的风险</strong>
          </p>
          <p class="MsoNormal">
          	融资租赁保证金是指为了担保或保证承租人全面及时履行支付租金等应付款项的义务而由出租人向承租人收取的金钱。保证金的性质和作用根据当事人的约定不同而不同，因此为避免歧义及产生纠纷，在订立保证金条款时应就保证金的作用、金额、支付方式、是否计息、保存及处置方式等各方面进行明确约定。
          </p>
          <p class="MsoNormal">
          	另外需要说明的是保证金可以与违约金或者定金共存，在汽车融资租赁合同中不能将保证金、违约金或者定金进行混淆，以免不能全面保护出租人利益。
          </p>
          <p class="MsoNormal">
          	应对措施：
          </p>
          <p class="MsoNormal">
          	1、在汽车融资租赁合同中，应明确约定保证金的保证范围应包含车辆修理费、过路费、运管费和车辆罚单款、年检、车船税、逾期未付的租金、保险费等应由承租人向第三方支付的其他应付费用，同时约定保证金一旦动用，乙方应于具体确定的日期内补足保证金金额，逾期未补足的即视为乙方根本违约;
          </p>
          <p class="MsoNormal">
          	2、在实务中，由于违约金金额受到造成的损失30%的上限限制，法院会根据实际情况作相应调整，而有些时候损失难以认定，因此约定违约定金以及保证金必不可少。
          </p>
          <p class="MsoNormal">
          	3、虽然违约定金与违约金只能择一而主张，但是并不是代表在实务中不可以同时约定违约定金与违约金。因此在约定违约定金的同时，还可在诸如车辆保养、年检配合等方面约定单次的违约金，发生纠纷时可选择适用，而且如此约定必然会对承租人在心理上造成压力，在一定程度上有利于保障合同的全面履行。
          </p>
          <p class="MsoNormal">
          	<strong> </strong><strong>(</strong><strong>四</strong><strong>)</strong><strong>车辆被无权处分的风险</strong>
          </p>
          <p class="MsoNormal">
          	在直租模式下，汽车融资租赁公司根据承租人的选择购买车辆后，将车辆登记于汽车融资租赁公司名下，车辆被无权处分的风险较小，但在售后回租模式下以及即便是基于直租模式，考虑到操作的便利性、税收成本以及后续车辆使用过程中的责任承担问题等因素。
          </p>
          <p class="MsoNormal">
          	应对措施：
          </p>
          <p class="MsoNormal">
          	1、避免将车辆权证如机动登记证、行驶证、机动车发票等登记于承租人名下;
          </p>
          <p class="MsoNormal">
          	2、无法避免时，在融资租赁合同中明确约定授权承租人将车辆抵押给汽车融资租赁公司并在登记机关依法办理抵押权登记;
          </p>
          <p class="MsoNormal">
          	3、在车辆的显著位置作出标识，足以让第三人在与承租人交易时知道或者应当知道该车辆为租赁车辆;
          </p>
          <p class="MsoNormal">
          	4、证明第三人不符合善意取得的要件;
          </p>
          <p class="MsoNormal">
          	5、根据《中华人民共和国最高人民法院关于审理融资租赁合同纠纷适用法律问题的解释》(以下简称“《融资租赁司法解释》”)第九条的规定，证明第三人属于负有交易时须按照法律、行政法规、行业或者地区主管部门的规定在相应机构进行融资租赁交易查询的义务主体。
          </p>
	        </div>
	      </div>
        <div v-if="index ==2" class="new_inner">
	            <h1 class="news_h1">商务部办公厅关于开展融资租赁业风险排查工作的通知</h1>
	            <h3 class="news_h3">发布时间：2017-05-09</h3>
	            <div class="newp">
                           <p class="MsoNormal" align="center" style="text-align:left;">
	            <span style="font-size:14px;text-indent:24pt;line-height:1.5;">各省、自治区、直辖市、计划单列市及新疆生产建设兵团商务主管部门：</span>
              </p>
              <p class="MsoNormal" align="center" style="text-indent:32px;text-align:left;">
              	<span style="text-indent:32.25pt;font-size:14px;">&nbsp;按照国务院有关工作部署，为有效防范和化解融资租赁行业风险隐患，规范市场秩序，促进行业健康发展，我部定于</span><span style="text-indent:32.25pt;font-size:14px;">5</span><span style="text-indent:32.25pt;font-size:14px;">月</span><span style="text-indent:32.25pt;font-size:14px;">2</span><span style="text-indent:32.25pt;font-size:14px;">日至</span><span style="text-indent:32.25pt;font-size:14px;">6</span><span style="text-indent:32.25pt;font-size:14px;">月</span><span style="text-indent:32.25pt;font-size:14px;">30</span><span style="text-indent:32.25pt;font-size:14px;">日组织各地开展融资租赁行业风险排查工作。现将有关事项通知如下：</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span></span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;">&nbsp;&nbsp;一、排查要点</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">（一）排查对象。</span></b><span style="text-indent:32.25pt;font-size:14px;">本次风险排查工作对象为所有内资融资租赁试点企业和外商投资融资租赁企业，对存在以下情况的企业要进行重点检查：</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">1.关联公司从事互联网金融、投资咨询、财富管理、第三方理财、小额贷款、融资担保、商业保理、典当等业务的企业。关联公司包括股东、股东投资的企业、同一实际控制人控制的其他企业及本公司所投资的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">2.售后回租项目承租人多为关联公司的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">3.股东或存在交易关系的关联公司及其高级管理人员近期出现过重大违法违规行为的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">4.业务规模短期内以超常规速度增长，风险资产比例、资产负债率和租金逾期率过高的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">5.主营业务占比偏低，存在大量对外投资和对外担保的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">6.以工业原材料、贵重金属等限制流通物，无形资产、生物资产、商业地产甚至住宅等作为主要租赁物的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">7.通过网络借贷平台等互联网金融企业进行融资，且融资规模较大的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">8.以自然人为承租人或业务合作对象，且近期发生过多次业务纠纷的企业（例如面向个人开展汽车融资租赁业务）。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">9.未按要求及时通过全国融资租赁企业管理信息系统填报相关信息的企业，或所填报信息明显存在不实、不准确等情况的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">10.注册地与实际经营地不一致、联系方式发生变化或已无法联系的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">11.取得经营资质后长期（超过一年）未开展业务的企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="text-indent:32.25pt;font-size:14px;">12.注册资本实到率偏低（不足</span><span style="text-indent:32.25pt;font-size:14px;">30%</span><span style="text-indent:32.25pt;font-size:14px;">）的企业，特别是注册资本实到率低但开展业务规模较大的外资企业。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span></span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:24pt;line-height:1.5;"><span style="font-size:14px;">（二）重点排查内容。</span></b>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">一是基本情况：</span></b>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">1.企业基本信息，包括但不限于股东或出资人、实际控制人、法定代表人、注册资本及实缴金额、分支机构数量及分布等。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">2.业务开展情况，包括承租人、租赁物及其权属状况、融资来源及方式、业务合规性、租金收取情况及逾期率等。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">3.境外借款、境外放款等资金跨境流动情况。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">二是存在的主要问题：</span></b>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">1.是否存在直接从事或参与吸收或变相吸收公众存款等行为；是否未经相关部门批准，从事同业拆借、股权投资等业务。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">2.是否违反国家有关规定向地方政府、地方政府融资平台公司提供融资或要求地方政府为租赁项目提供担保、承诺还款等。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">3.是否存在虚构租赁物、以不符合法律规定的标的为租赁物、未实际取得租赁物所有权或租赁物合同价值与实际价值明显不符，以融资租赁为名义实际从事资金融通业务甚至变相发放贷款等行为。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">4.是否存在与关联公司之间进行租赁物低值高买、高值低租等明显不符合市场规律的交易行为。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">6.是否存在虚假宣传（例如宣称具有金融牌照、以金融机构名义进行宣传等）、故意虚构融资租赁项目通过公开渠道（如互联网金融平台）进行融资等行为。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">7.是否存在超杠杆经营，即风险资产比例是否超过规定的限额。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">8.是否按要求及时报送季度和年度经营情况信息报表，在全国融资租赁企业管理信息系统上登记的信息是否真实准确。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">9.外商投资融资租赁企业是否按要求及时进行外商投资企业设立及变更备案，是否参加外商投资企业年度投资经营信息联合报告（联合年报）工作。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">（三）排查方式。</span></b><span style="text-indent:32.25pt;font-size:14px;">各地商务主管部门可根据工作需要，采取多种措施开展排查工作。对于跨区域经营的企业，注册所在地和经营所在地商务主管部门要互通信息，加强合作，防止出现排查空白。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">1.&nbsp;企业自查。要求企业开展风险自查，提交自查报告，针对自查发现的问题和风险隐患及时进行整改。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="text-indent:32.25pt;font-size:14px;">2.&nbsp;信息化监管。通过全国融资租赁企业管理信息系统对企业填报的交易记录、经营信息、财务数据等数据进行分析，查找风险点和违法违规活动线索，核对系统填报信息的真实性与准确性。督促企业按照《融资租赁企业监督管理办法》（商流通发〔</span><span style="text-indent:32.25pt;font-size:14px;">2013</span><span style="text-indent:32.25pt;font-size:14px;">〕</span><span style="text-indent:32.25pt;font-size:14px;">337</span><span style="text-indent:32.25pt;font-size:14px;">号）的要求，及时、准确填报全国融资租赁企业管理信息系统。对不及时填报、瞒报或虚报信息的企业，要求其立即整改，对于不按要求整改的企业，建立企业报送信息异常名录并报我部，我部将适时通过适当方式进行公开。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">3.&nbsp;现场检查。抽取一定比例的企业进行现场检查，重点检查企业财务记录、银行对账单、业务合同、融资合同或凭证等反映资金来源和流向的材料，实地抽查租赁物及其相关权利凭证确认租赁物及其权属，判断租赁项目的真实性，检查重复抵押、租赁物所有权保护、资金监管等方面是否存在风险隐患。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">4.&nbsp;人员约谈。视情况需要约谈企业股东、高级管理人员、财务人员或其他员工，了解经营情况，加强风险教育，查找违法违规线索。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">5.&nbsp;外部调研。必要时与承租人进行沟通，了解融资租赁企业经营合规情况、项目的真实合规性，查找违法违规线索。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">6.&nbsp;第三方协助。必要时可聘请会计师事务所、律师事务所或委托行业协会等机构协助排查。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">7.&nbsp;其他合法方式。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<span style="font-size:14px;text-indent:32.25pt;line-height:1.5;">二、工作要求</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">（一）落实责任，主动作为。</span></b><span style="text-indent:32.25pt;font-size:14px;">各地商务主管部门要高度重视风险排查工作，切实落实属地监管责任，把此次风险排查工作列入重要工作日程，尽快部署专项排查活动，制定详细的检查工作方案，明确分工职责和阶段部署，切实抓好落实，确保检查工作不走过场。内资试点企业和外商投资企业由相关处室分别负责。参与检查人员应当客观公正，实事求是，忠诚履职，廉洁奉公，保守秘密。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">（二）积极稳妥，分类施策。</span></b><span style="text-indent:32.25pt;font-size:14px;">排查和处置工作要严格依法，讲究策略，对于排查出的线索，综合考虑风险性质、社会危害等因素，制定差别化的处置策略，分类化解。对于检查中发现的经营管理不规范问题，应要求企业限期改正。对于重大违法违规行为线索，应及时提请本级相关执法部门予以处理。对于检查中发现的普遍性、系统性风险问题，应及时采取通报、风险提示等措施。对于监管体制机制存在的问题，应作出修改或提出完善建议。要制定完善突发事件应对预案，明确非法集资等重大风险应对的责任主体、触发情形、风险评估、响应处置等内容和措施。对于检查中发现的可能引发重大突发事件的潜在风险问题，应及时向当地人民政府报告，并报我部。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">（三）源头治理，长效监管。</span></b><span style="text-indent:32.25pt;font-size:14px;">一是加强规制建设、监管检查和监测预警，防打结合，以防为主，坚持风险早发现、早预警、早处置。二是结合排查工作对企业使用全国融资租赁企业管理信息系统的情况进行督促检查，及时了解企业经营状况、合规情况，梳理失联企业名单及有关情况，建立企业报送信息异常名录。三是强化日常监管制度，着力完善融资租赁行业监管制度，稳妥解决体制性、机制性、规制性问题，强化防控风险长效机制，加强与金融、税务、公安、工商等部门间的沟通协调机制，强化信息共享与监管合作。对于此次检查中发现问题较为突出的企业，要将其列入重点监管对象。研究建立监管评级制度，对融资租赁企业进行分类管理。加强行业组织建设，充分发挥行业自律作用。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:24pt;">
              	<b style="text-indent:32.25pt;line-height:1.5;"><span style="font-size:14px;">（四）总结经验，及时报告。</span></b><span style="text-indent:32.25pt;font-size:14px;">各地商务主管部门要对此次风险排查中发现的情况进行全面分析，综合研判本地融资租赁业的发展现状与潜在问题，从以下方面形成排查情况报告：一是风险排查工作组织实施情况；二是排查中发现的风险问题及应对措施（内容要具体化，尽可能通过列举事例的方式进行分析）；三是本地融资租赁行业发展现状及主要风险因素；四是下一步强化事中事后监管、风险防范预警、建立长效机制的工作安排与建议；五是失联企业名单（作为附件）。请各地商务主管部门将上述内容形成书面报告，并于</span><span style="text-indent:32.25pt;font-size:14px;">7</span><span style="text-indent:32.25pt;font-size:14px;">月</span><span style="text-indent:32.25pt;font-size:14px;">15</span><span style="text-indent:32.25pt;font-size:14px;">日前报送我部（一式两份，分别报送流通发展司、外资司）。</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span></span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span style="font-size:14px;">联系人：流通发展司：王巧璐</span><span style="font-size:14px;">&nbsp;010-85093746</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:73.5pt;">
              	<span style="font-size:14px;">外资司</span><span style="font-size:14px;">&nbsp;</span><span style="font-size:14px;">：</span><span style="font-size:14px;">&nbsp;</span><span style="font-size:14px;">张澜</span><span style="font-size:14px;">&nbsp;&nbsp;010-65197982</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:96pt;">
              	<span style="font-size:14px;">&nbsp;</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span style="font-size:14px;">&nbsp;</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span style="font-size:14px;">&nbsp;</span>
              </p>
              <p class="MsoNormal" align="left" style="text-indent:32.25pt;">
              	<span style="font-size:14px;">&nbsp;</span>
              </p>
              <p class="MsoNormal" align="right" style="margin-left:0cm;text-align:right;text-indent:32.25pt;">
              	<span style="font-size:14px;">&nbsp;&nbsp;商务部办公厅</span><span></span>
              </p>
              <p class="MsoNormal" align="right" style="margin-left:0cm;text-align:right;text-indent:32.25pt;">
              	<span style="font-size:14px;">2017年</span><span style="font-size:14px;">5</span><span style="font-size:14px;">月</span><span style="font-size:14px;">2</span><span style="font-size:14px;">日</span><span></span>
              </p>
              <p class="MsoNormal" align="right" style="margin-left:0cm;text-align:right;text-indent:32.25pt;">
              	<span style="text-indent:10px;white-space:normal;font-size:14px;">文章来源：商务部流通业发展司</span>
              </p>
	          </div>
	      </div>   
        <div v-if="index ==3" class="new_inner">
              	<h1 class="news_h1">很多人都会询问：什么样的企业适合融资租赁？</h1>
              	<h3 class="news_h3">发布时间：2017-05-09</h3>
              	<div class="newp">
                      <p class="MsoNormal" align="center" style="text-align:left;">
              	&nbsp; &nbsp; &nbsp;&nbsp;<img src="/uploadfiles/image/20170509/20170509145622_8941.jpg" align="left" alt=""><span style="font-size:14px;line-height:1.5;">通俗的说法就是，如果企业想生产产品，但是买设备的钱不够，在这种情况下融资租赁就能发挥决定性作用。</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;一般是</span><span lang="EN-US" style="font-size:14px;">3</span><span style="font-size:14px;">至</span><span lang="EN-US" style="font-size:14px;">5</span><span style="font-size:14px;">年，融资额度从几十万元到上亿元，弹性很大。而融资租赁则成为中小企业重要的融资方式，中小企业融资租赁的意义又是什么？</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;借助融资租赁的杠杆可助推生产企业转型升级，据专家介绍，融资租赁具有融资与融物相结合的特点，在办理融资时对企业资信和担保的要求不高，非常适合中小企业融资。</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;此外，融资租赁属于表外融资，不体现在企业财务报表的负债项目中，不影响企业的资信状况。这对需要多渠道融资的中小企业而言非常有利。</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;融资租赁是指具有融资性质和所有权转移特点的设备租赁业务。即：出租人根据承租人所要求的规格、型号、性能等条件购入设备租赁给承租人，合同期内设备所有权属于出租人，承租人只拥有使用权，合同期满付清租金后，承租人有权按残值购入设备，拥有设备的所有权。</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;融资租赁的优势</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;一、</span><span style="font-size:14px;line-height:1.5;">对企业的好处</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;1、</span><span style="font-size:14px;line-height:1.5;">拓宽融资渠道、操作快捷</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;融资租赁通过“融物”方式实现“融资”目的。对于企业而言则提供了一条新的融资途径，拓宽了企业融资渠道。银行贷款的特点是门槛较高、审查严格、程序较长、手续较繁、额度有限，特别对于一些新设立企业、中小企业由于信用状况较差，很难获得银行贷款资金支持。而融资信用审核手续简便、操作快捷，资金能很快到位。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;2、</span><span style="font-size:14px;line-height:1.5;">资金使用灵活</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;较之于其他融资方式，采用租赁融资对提供给企业的资金监管较为宽松，有利于企业进行灵活的资金安排（主要体现在售后回租交易中，由于是通过出售资产取得的资金，企业可以自由使用该资金）。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;3、</span><span style="font-size:14px;line-height:1.5;">不占用企业授信额度</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;企业通过商务部融资租赁试点租赁企业获得的资金不会计入人行征信系统，不占用企业在银行授信额度，有利于企业通过租赁 公司融资平台与银行开展全方位、深层次的创新合作。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;4、</span><span style="font-size:14px;line-height:1.5;">提高企业经营灵活性</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;经营性租赁具有租赁方式灵活，可随时退租的特点，企业选择这种方式引进固定资产，可以在市场条件好的时候迅速扩大生产规模，在市场萎缩时灵活退出，有利于提高企业经营的灵活性。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;5、</span><span style="font-size:14px;line-height:1.5;">改善财务报表</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;与银行贷款或外国政府贷款方式不同，融资租赁属于表外融资，融资租赁的租金不体现在财务报表的负债项目中，融资租赁的租金在财务管理中可以税前列支。承租人采用融资租赁方式租入固定资产时，一般可获得</span><span lang="EN-US" style="font-size:14px;">3</span><span style="font-size:14px;">～</span><span lang="EN-US" style="font-size:14px;">5</span><span style="font-size:14px;">年的中长期融资，
              相比采用银行流动资金贷款或短期商业信用而言，既能改善流动比率、速动比率等短期偿债能力指标，也可以相对降低承租人资产负债率</span><span lang="EN-US" style="font-size:14px;">(</span><span style="font-size:14px;">保留或提高承租人的融资能力</span><span lang="EN-US" style="font-size:14px;">)</span><span style="font-size:14px;">、提高资产收益率指标等。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;6、</span><span style="font-size:14px;line-height:1.5;">回避政策性、市场性限制</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;很多单位在购置固定资产时存在不同方面的政策限制，有些来自监管部门，有些来自总部内部管理制度的控制，有些来自市场信息披露等运作的障碍。如各类银行、信用社、国家资产管理公司、保险公司、上市公司、集团分公司等采用融资租赁业务，可以有效的回避这些限制。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;7、</span><span style="font-size:14px;line-height:1.5;">加速折旧，具有节税功能</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;根据财政部、国家税务总局有关文件规定，“企业技术改造采取融资租赁方式租入的机器设各，折旧年限可按租赁期限和国家规定的折旧年限孰短的原则确定，但最短折旧年限不短于三年”，间接地起到了加速折旧的作用。企业可以按照最有利的原则，尽快折旧，把折旧费用打入成本。与税后还贷相比，显然对企业有利。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;8、</span><span style="font-size:14px;line-height:1.5;">到期还本负担较轻</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;银行贷款一般是采用整笔贷出，整笔归还。而租赁公司却可以根据每个企业的资金实力、销售季节性等具体情况，为企业定做灵活的还款安排，例如延期支付，递增和递减支付等，使承租人能够根据自己的企业状况定制付款额。</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;二、</span><span style="font-size:14px;line-height:1.5;">对银行的好处</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;1、</span><span style="font-size:14px;line-height:1.5;">风险防火墙</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;一般而言，租赁公司是租赁物件的法定所有权人，这样就形成了一定的风险隔离，若出现承租人破产的情况出租人可直接收回和处置租赁物。同时，在租赁结构设计上，租赁公司也会采用相应的外部增信手段对租赁项目进行增信，以控制风险。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;2、</span><span style="font-size:14px;line-height:1.5;">为优质客户提供更大规模的资金支持</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;银行由于受到单一客户集中度的限制，对其优质客户的授信也受到一定的限制，通过租赁公司作为贷款主体，能够给优质客户提供更多的资金支持。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;3、</span><span style="font-size:14px;line-height:1.5;">增加银行中间业务</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;通过发行理财产品融资、应收账款保理、利率掉期等形式可增加银行中间业务收入。</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;三、</span><span style="font-size:14px;line-height:1.5;">对政府（平台公司）的好处</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;1、</span><span style="font-size:14px;line-height:1.5;">拓宽融资渠道</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;可通过租赁开辟新的融资渠道，且租赁资金使用灵活，可以充当资本金使用，这样对于政府筹集基础设施建设项目资本金（在基础设施建设项目中必需有一定比例的资本金才能够获得银行贷款支持）有突出的贡献。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;2、</span><span style="font-size:14px;line-height:1.5;">盘活固定资产，提高资金使用效率</span> 
              </p>
              <p class="MsoNormal">
              	<span style="font-size:14px;">通过售后回租模式，盘活政府已投入固定资产（管网、大楼等），释放政府前期投入资金，能够使政府有更多的资金进行固定资产再投资。同时通过租赁的财务杠杆作用，带来投资乘数效应。</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;3、</span><span style="font-size:14px;line-height:1.5;">改善财务报表</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;4、</span><span style="font-size:14px;line-height:1.5;">回避政策性、市场性限制</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;5、</span><span style="font-size:14px;line-height:1.5;">加速折旧，具有节税功能</span> 
              </p>
              <p class="MsoNormal">
              	<span lang="EN-US" style="font-size:14px;">&nbsp; &nbsp; &nbsp; &nbsp;6、</span><span style="font-size:14px;line-height:1.5;">到期还本负担较轻</span> 
              </p>
              <p class="MsoNormal" style="text-align:right;">
              	<span style="font-size:14px;"><br>
              </span> 
              </p>
              <p class="MsoNormal" style="text-align:right;">
              	<span style="font-size:14px;">以上信息来自于网络</span> 
              </p>
              <p class="MsoNormal" align="right" style="text-align:right;text-indent:21.0pt;">
              	<span lang="EN-US" style="font-size:14px;">&nbsp;</span> 
              </p>
              <p class="MsoNormal" align="right" style="text-align:right;text-indent:21.0pt;">
              	<span lang="EN-US" style="font-size:14px;">&nbsp;</span> 
              </p>
              <p class="MsoNormal" align="right" style="text-align:right;text-indent:21.0pt;">
              	<span lang="EN-US" style="font-size:14px;">&nbsp;</span> 
              </p>
              <span style="font-size:14px;"></span> 
              <p>
              	<br>
              </p>
              	</div>
	      </div>
        <div v-if="index ==4" class="new_inner">
            	<h1 class="news_h1">控制风险，融资租赁必知的3种风控模式</h1>
            	<h3 class="news_h3">发布时间：2017-06-06</h3>
            	<div class="newp">
                   <p class="MsoNormal" align="left" style="margin:18pt 0cm;line-height:18pt;">
            	&nbsp; &nbsp; &nbsp; &nbsp;融资租赁行业是一个高风险的行业，经营理念上必须坚持风险控制第一的原则，必须在风险可控的前提下来谋求业务的发展。特别是在今朝的经济状态下：全球经济刚刚走过金融危机，中国国内经济增速回落，许多企业转向融资租赁这一模式来缓和自身供应链的紧张，融资租赁的业务量呈现出逆势向上的态势。但在业务量节节攀升的时候，我们更要审慎度势，把好风险管理的关隘。融资租赁作为高风险行业，其租赁业务风险控制能力在很大程度上决定企业的经营业绩。风险控制是融资租赁业务的重要组成部分，是企业需要关注并持续改进的管理重点。<o:p></o:p>
            </p>
            <p class="MsoNormal" align="left" style="margin:18pt 0cm;line-height:18pt;">
            	一、全程风控<o:p></o:p>
            </p>
            <p class="MsoNormal" align="left" style="margin:18pt 0cm;line-height:18pt;">
            	&nbsp; &nbsp; &nbsp; 全程风控，就是从业务扩展、市场营销、客户信息管理、尽职调查一直到项目审批、合同管理、租后的资产管理以及合规性管理，租赁业务操作的全过程，风险控制都一环不漏，层层把关。融资租赁企业可利用信息化手段，通过客户端、邮件等移动办公手段，使员工无论身处何地，都能随时参与整个融资租赁业务的全过程，如客户授信资质确认、租赁物现状查询、项目进度跟进、租后租金管理等等，通过业务流程将整个融资租赁业务过程串联起来，并借助留痕控制、权限管理等工具，加强过程管理的效果。<o:p></o:p>
            </p>
            <p class="MsoNormal" align="left" style="margin:18pt 0cm;line-height:18pt;">
            	二、全员风控<o:p></o:p>
            </p>
            <p class="MsoNormal" align="left" style="margin:18pt 0cm;line-height:18pt;">
            	&nbsp; &nbsp; &nbsp;&nbsp;全员风控，就是指不仅业务一线人员，如客户经理、项目经理等、业务二线风控人员，如风控经理、评审委员等需要特别进行风险控制，公司的其他人员，如财务人员、行政人员等，也应从不同角度、不同的信息渠道关注公司业务经营的风险。融资租赁的风险控制体系要与公司组织架构、企业管理制度、业务流程紧密的联系在一起，明确每个部门的具体职责与业务流程，如开发项目的人不得参与审批，财务部门不能管理业务，管理项目的人不能管理业务开发等，发挥各部门员工的风控意识，将企业的风控理念通过流程内化到每个员工的日常工作，全体动员，加强风控。<o:p></o:p>
            </p>
            <p class="MsoNormal" align="left" style="margin:18pt 0cm;line-height:18pt;">
            	三、全面风控<o:p></o:p>
            </p>
            <p class="MsoNormal" align="left" style="margin:18pt 0cm;text-indent:21pt;line-height:18pt;">
            	融资租赁是金融和贸易结合的边缘产业，涉及面比较广，是个系统工程，风险控制也是系统工程。融资租赁的风险控制必须建立在产业链的基础之上，充分利用相关政府部门的管理职能，有效整合融资租赁公司、厂商和担保、保险等融资租赁中介等租赁产业链的各方优势，资源互补，将事前风险分析、事中项目控制、租后资产监督等过程环环相扣，从财务、业务、资产和收益多视角调研、判断与监督。通过科学的融资租赁项目结构和规范的业务操作流程，依托完善的企业内部管理机制，将融资租赁的内外部风险牢牢掌握，实现全面风控。<o:p></o:p>
            </p>
            	</div>
	      </div> 
        <div v-if="index ==5" class="new_inner">
                	<h1 class="news_h1">外商投资租赁业管理办法</h1>
                	<h3 class="news_h3">发布时间：2017-05-27</h3>
                	<div class="newp">
                        <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp; 第一条 为促进外商投资租赁业的健康发展，规范外商投资租赁业的经营行为，防范经营风险，根据《中华人民共和国合同法》、《中华人民共和国公司法》、《中华人民共和国外资企业法》、《中华人民共和国中外合资经营企业法》、《中华人民共和国中外合作经营企业法》等有关法律、法规，制定本办法。
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp; 第二条 外国公司、企业和其他经济组织（以下简称外国投资者）在中华人民共和国境内以中外合资、中外合作以及外商独资的形式设立从事租赁业务、融资租赁业务的外商投资企业，开展经营活动，适用本办法。
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp; 第三条 外商投资租赁业可以采取有限责任公司或股份有限公司的形式。<span style="line-height:1.5;">&nbsp;</span>
                </p>
                <p class="MsoNormal">
                	从事租赁业务的外商投资企业为外商投资租赁公司；从事融资租赁业务的外商投资企业为外商投资融资租赁公司。<span style="line-height:1.5;">&nbsp;</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp; 第四条 外商投资租赁公司及外商投资融资租赁公司应遵守中华人民共和国有关法律、法规及规章的规定，其正当经营活动及合法权益受中国法律保护。<span lang="EN-US"><o:p></o:p></span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">商务部是外商投资租赁业的行业主管部门和审批管理部门。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第五条 本办法所称租赁业务系指出租人将租赁财产交付承租人使用、收益，并向承租人收取租金的业务。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">本办法所称融资租赁业务系指出租人根据承租人对出卖人、租赁物的选择，向出卖人购买租赁财产，提供给承租人使用，并向承租人收取租金的业务。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">外商投资融资租赁公司可以采取直接租赁、转租赁、回租赁、杠杆租赁、委托租赁、联合租赁等不同形式开展融资租赁业务。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第六条 本办法所称租赁财产包括：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）生产设备、通信设备、医疗设备、科研设备、检验检测设备、工程机械设备、办公设备等各类动产；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）飞机、汽车、船舶等各类交通工具；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（三）本条（一）、（二）项所述动产和交通工具附带的软件、技术等无形资产，但附带的无形资产价值不得超过租赁财产价值的二分之一。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第七条 外商投资租赁公司和外商投资融资租赁公司的外国投资者的总资产不得低于</span><span lang="EN-US" style="line-height:1.5;">500</span><span style="line-height:1.5;">万美元。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第八条 外商投资租赁公司应当符合下列条件：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）注册资本符合《公司法》的有关规定；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）符合外商投资企业注册资本和投资总额的有关规定；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（三）有限责任公司形式的外商投资租赁公司的经营期限一般不超过</span><span lang="EN-US" style="line-height:1.5;">30</span><span style="line-height:1.5;">年。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第九条 外商投资融资租赁公司应当符合下列条件：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）有限责任公司形式的外商投资融资租赁公司的经营期限一般不超过</span><span lang="EN-US" style="line-height:1.5;">30</span><span style="line-height:1.5;">年。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）拥有相应的专业人员，高级管理人员应具有相应专业资质和不少于三年的从业经验。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十条 设立外商投资租赁公司和外商投资融资租赁公司应向审批部门报送下列材料：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）申请书；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）投资各方签署的可行性研究报告；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（三）合同、章程（外资企业只报送章程）；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（四）投资各方的银行资信证明、注册登记证明（复印件）、法定代表人身份证明（复印件）；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（五）投资各方经会计师事务所审计的最近一年的审计报告；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（六）董事会成员名单及投资各方董事委派书；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（七）高级管理人员的资历证明；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（八）工商行政管理部门出具的企业名称预先核准通知书；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">申请成立股份有限公司的，还应提交有关规定要求提交的其他材料。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十一条 设立外商投资租赁公司和外商投资融资租赁公司，应按照以下程序办理：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）设立有限责任公司形式的外商投资租赁公司，应由投资者向拟设立企业所在地的省级商务主管部门报送本办法第十条规定的全部材料，省级商务主管部门应自收到全部申请材料之日起</span><span lang="EN-US" style="line-height:1.5;">45</span><span style="line-height:1.5;">个工作日内做出是否批准的决定，批准设立的，颁发《外商投资企业批准证书》，不予批准的，应书面说明原因。省级商务主管部门应当在批准外商投资租赁公司设立后</span><span lang="EN-US" style="line-height:1.5;">7</span><span style="line-height:1.5;">个工作日内将批准文件报送商务部备案。股份有限公司形式的外商投资租赁公司的设立按照有关规定办理。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）设立外商投资融资租赁公司，应由投资者向拟设立企业所在地的省级商务主管部门报送本办法第十条规定的全部材料，省级商务主管部门对报送的申请文件进行初审后，自收到全部申请文件之日起</span><span lang="EN-US" style="line-height:1.5;">15</span><span style="line-height:1.5;">个工作日内将申请文件和初审意见上报商务部。商务部应自收到全部申请文件之日起</span><span lang="EN-US" style="line-height:1.5;">45</span><span style="line-height:1.5;">个工作日内做出是否批准的决定，批准设立的，颁发《外商投资企业批准证书》，不予批准的，应书面说明原因。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（三）已设立的外商投资企业申请从事租赁业务的，应当符合本办法规定的条件，并按照本条第（一）项规定的程序，依法变更相应的经营范围。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十二条 外商投资租赁公司和外商投资融资租赁公司应当在收到《外商投资企业批准证书》之日起</span><span lang="EN-US" style="line-height:1.5;">30</span><span style="line-height:1.5;">个工作日内到工商行政管理部门办理登记注册手续。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十三条 外商投资租赁公司可以经营下列业务：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）租赁业务；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）向国内外购买租赁财产；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（三）租赁财产的残值处理及维修；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（四）经审批部门批准的其他业务。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十四条 外商投资融资租赁公司可以经营下列业务：</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（一）融资租赁业务；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（二）租赁业务；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（三）向国内外购买租赁财产；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（四）租赁财产的残值处理及维修；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（五）租赁交易咨询和担保；</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">（六）经审批部门批准的其他业务。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十五条 外商投资融资租赁公司根据承租人的选择，进口租赁财产涉及配额、许可证等专项政策管理的，应由承租人或融资租赁公司按有关规定办理申领手续。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">外商投资租赁公司进口租赁财产，应按现行外商投资企业进口设备的有关规定办理。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十六条 为防范风险，保障经营安全，外商投资融资租赁公司的风险资产一般不得超过净资产总额的</span><span lang="EN-US" style="line-height:1.5;">10</span><span style="line-height:1.5;">倍。风险资产按企业的总资产减去现金、银行存款、国债和委托租赁资产后的剩余资产总额确定。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十七条 外商投资融资租赁公司应在每年</span><span lang="EN-US" style="line-height:1.5;">3</span><span style="line-height:1.5;">月</span><span lang="EN-US" style="line-height:1.5;">31</span><span style="line-height:1.5;">日之前向商务部报送上一年业务经营情况报告和上一年经会计师事务所审计的财务报告。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十八条 中国外商投资企业协会租赁业委员会是对外商投资租赁业实行同业自律管理的行业性组织。鼓励外商投资租赁公司和外商投资融资租赁公司加入该委员会。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第十九条 外商投资租赁公司及外商投资融资租赁公司如有违反中国法律、法规和规章的行为，按照有关规定处理。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第二十条 香港特别行政区、澳门特别行政区、台湾地区的公司、企业和其他经济组织在内地设立外商投资租赁公司和外商投资融资租赁公司，参照本办法执行。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第二十一条 本办法中所称省级商务主管部门是指各省、自治区、直辖市、计划单列市及新疆生产建设兵团商务主管部门。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第二十二条 本办法由商务部负责解释。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp; &nbsp; &nbsp;&nbsp;<span style="line-height:1.5;">第二十三条 本办法自二○○五年三月五日起施行。原外经贸部</span><span lang="EN-US" style="line-height:1.5;">2001</span><span style="line-height:1.5;">年第</span><span lang="EN-US" style="line-height:1.5;">3</span><span style="line-height:1.5;">号令《外商投资租赁公司审批管理暂行办法》同时废止。</span>
                </p>
                <p class="MsoNormal">
                	&nbsp;
                </p>
                	</div>
	      </div> 
        <div v-if="index ==6" class="new_inner ">
          <img src="../../assets/img/new1.jpg"  style="margin: 0 auto;    display: block;" alt="">
          <img src="../../assets/img/new2.jpg"  style="margin: 0 auto;    display: block;" alt="">
          <img src="../../assets/img/new3.jpg" style="margin: 0 auto;    display: block;" alt="">
          <img src="../../assets/img/new4.jpg" style="margin: 0 auto;    display: block;" alt="">
          <img src="../../assets/img/new5.jpg" style="margin: 0 auto;    display: block;" alt="">
          <img src="../../assets/img/new6.jpg" style="margin: 0 auto;    display: block;" alt="">
        </div>                           
      </el-dialog>
      </el-row>
    </div>
</template>
<script>
import bus from "./bus";
import vHeader from "@/components/common/header.vue";
import vMap from "@/components/common/map.vue";
export default {
  data() {
    return {
      business: [
        {
          class: "",
          title: "交通运输",
          detail: "Industrial Equipment Sector",
          show: true,
          p:
            "依托 良好合作及产品品牌优势 整合公司资源 寻求真诚合作 提供专业快捷、差异化的全方位融资解决方案。"
        },
        {
          class: "x1_ico2",
          title: "工业装备",
          detail: "Agricultural Industry Sector",
          show: true,
          p:
            "提供机床等工业加工设备的融资租赁产品，同时帮助拓展潜在市场。目前涉及等众多领域，寻求与国内外知名设备厂商、销售商、企业、协会等合作伙伴建立长期良好的合作关系。"
        },
        {
          class: "x1_ico3",
          title: "3C  数码",
          detail: "3C digita Sector",
          show: true,
          p:
            "一方面帮助普通用户低成本获取高客单价的3C装备，另一方面为拥有高客单价3C装备的个人提供产品托管和租赁业务。"
        },
        {
          class: "x1_ico4",
          title: "医疗设备",
          detail: "Medical Equipment Sector",
          show: true,
          p:
            "以大型医疗设备、数字手术设备、洁净工程等为核心产品，与目标医院逐个建立合作关系，为厂家、合作伙伴及医院提供直接或间接的融资租赁服务。"
        }
      ],
      new2: [
        {
          src: require("../../assets/img/hyzx1.jpg"),
          title: "汽车融资租赁中的风险点及其应对措施",
          detail:
            "引导语：汽车融资租赁，是指融资租赁公司根据承租人对租赁车辆与供应商的选择，与供应商签订《车辆买卖合同》购买相应车辆并根据其与承租人签订的《融资租赁合同》出租给承租人使用，承租人分期向融资租赁公司支付租金，租赁期满，租金付讫后，出租人将租赁车辆以象征性的价格无条件过户给承租人的交易行为。...",
          time: "2017-08-03"
        },
        {
          src: require("../../assets/img/hyzx2.jpg"),
          title: "商务部办公厅关于开展融资租赁业风险排查工作的通知",
          detail:
            "各省、自治区、直辖市、计划单列市及新疆生产建设兵团商务主管部门：按照国务院有关工作部署，为有效防范和化解融资租赁行业风险隐患，规范市场秩序，促进行业健康发展，我部定于5月2日至6月30日组织各地开展融资租赁行业风险排查工作。现将有关事项通知如下： 一、排查要点（...",
          time: "2017-05-09"
        },
        {
          src: require("../../assets/img/hyzx3.jpg"),
          title: "很多人都会询问：什么样的企业适合融资租赁？",
          detail:
            "通俗的说法就是，如果企业想生产产品，但是买设备的钱不够，在这种情况下融资租赁就能发挥决定性作用。一般是3至5年，融资额度从几十万元到上亿元，弹性很大。而融资租赁则成为中小企业重要的融资方式，中小企业融资租赁的意义又是什么？借助融资租赁的杠杆可助推生产企...",
          time: "2017-08-03"
        }
      ],
      new3: [
        {
          src: require("../../assets/img/flfg1.jpg"),
          title: "控制风险，融资租赁必知的3种风控模式",
          detail:
            "融资租赁行业是一个高风险的行业，经营理念上必须坚持风险控制第一的原则，必须在风险可控的前提下来谋求业务的发展。特别是在今朝的经济状态下：全球经济刚刚走过金融危机，中国国内经济增速回落，许多企业转向融资租赁这一模式来缓和自身供应链的紧张，融资租赁的业务量呈现出逆势向上的态势。但在业...",
          time: "2017-06-06"
        },
        {
          src: require("../../assets/img/flfg2.jpg"),
          title: "外商投资租赁业管理办法",
          detail:
            "第一条 为促进外商投资租赁业的健康发展，规范外商投资租赁业的经营行为，防范经营风险，根据《中华人民共和国合同法》、《中华人民共和国公司法》、《中华人民共和国外资企业法》、《中华人民共和国中外合资经营企业法》、《中华人民共和国中外合作经营企业法》等有关法律、法规，制定本办法。",
          time: "2017-05-09"
        },
        {
          src: require("../../assets/img/flfg3.jpg"),
          title: "融资租赁企业监督管理办法",
          detail: "",
          time: "2017-05-04"
        }
      ],
      fix: false,
      man: false,
      show: false,
      dialogVisible: false,
      index: 0
    };
  },
  created() {
    bus.$on("collapse", msg => {
      let ms = msg;
      let top = document.getElementById(ms).offsetTop - 70;
      // window.scrollTo(0, `${top}`);

      jQuery("html,body").animate({ scrollTop: `${top}px` }, 800);
    });
    bus.$on("collaps", msg => {
      this.fix = msg;
      console.log(msg);
    });
    bus.$on("man", msg => {
      this.man = msg;
    });
  },
  components: {
    vMap,
    vHeader
  },
  methods: {
    sho(show, index) {
      console.log(index);
      this.business[index].show = !show;
    },
    showIndex(index) {
      this.dialogVisible = true;
      this.index = index;
    }
  }
};
</script>
<style>
#el .el-dialog__header {
  display: none;
}
</style>

<style lang="scss" scoped>
.fix {
  display: none;
}

.fixx {
  position: fixed;
}
.ind_bt {
  font: 24px/24px "Arial";
  color: #666666;
  text-align: center;
}
.col-flex {
  height: 250px;
}
.ind_btcha {
  text-align: center;
  margin-bottom: 20px;
  color: rgb(51, 51, 51);
  font: 18px/36px 微软雅黑;
  background: url(../../assets/img/ind_01.png) center center no-repeat;
}
.margin {
  .ind_box1 {
    padding: 70px 0;
    text-align: center;
    overflow: hidden;
    zoom: 1;
    .col-flex {
      display: flex;
      justify-content: space-between;
    }
    .x1:hover {
      background-color: #197c56;
    }
    .x1 {
      display: block;
      width: 230px;
      height: 250px;
      background: #5c5c5c url(../../assets/img/ind_03.png) no-repeat center
        210px;
      position: absolute;
      top: 0;
      left: 0;
      .x1_ico {
        margin-top: 46px;
        width: 71px;
        height: 70px;
        background: url(../../assets/img/ico.png) no-repeat -1px -37px;
        display: inline-block;
      }
      .x1_bt {
        margin-top: 32px;
        color: rgb(255, 255, 255);
        font: 18px/18px 微软雅黑;
      }
      .x1_bteng {
        font: 11px/36px "Arial";
        color: #fff;
        letter-spacing: 0.5px;
        filter: alpha(opacity=80);
        opacity: 0.8;
      }
      .x1_ico2 {
        background-position: -1px -122px;
      }
      .x1_ico3 {
        background-position:-166px -296px;
      }
      .x1_ico4 {
        background-position: -1px -275px;
      }
    }
  }
}
.ind_box2 {
  width: 100%;
  height: 476px;
  padding-top: 50px;
  background: url(../../assets/img/ind_04.jpg) no-repeat center;
  .ind_btcha {
    margin-bottom: 70px;
  }
  .ind_x2 {
    width: 1004px;
    padding-right: 30px;
    height: 350px;
    margin: 0 auto -45px;
    background: #197c56;
  }
  .x2_bt {
    color: rgb(255, 255, 255);
    margin-bottom: 10px;
    font: 24px/112px 微软雅黑;
    background: url(../../assets/img/ind_05.png) 550px 93px no-repeat;
  }
  .x2_sm {
    color: rgb(255, 255, 255);
    opacity: 0.6;
    height: 152px;
    font: 12px/20px 微软雅黑;
  }
  .x2_ico {
    float: left;
    width: 20px;
    height: 20px;
    margin-right: 9px;
    background: url(../../assets/img/ico.png) no-repeat -88px 0;
  }
  .x2_img {
    margin: -32px 30px 0 27px;
    float: left;
  }
}
.ind_box3 {
  padding-top: 115px;
  height: 475px;
  .k1 {
    width: 1100px;
    margin: 0 auto;
  }
  .left {
    width: 360px;
  }
  .l {
    float: left;
  }
  .right {
    width: 660px;
  }
  .r {
    float: right;
  }
  .left_bt {
    color: #333333;
    font: 14px/52px "微软雅黑";
  }
  .left_sm {
    color: #666666;
    font: 12px/18px "微软雅黑";
  }
  .num {
    font: 80px/80px "Arial";
    color: #666666;
    filter: alpha(opacity=50);
    opacity: 0.5;
  }
  .wz {
    width: 470px;
  }
  .x3_bt {
    font: 14px/36px "微软雅黑";
    color: #333333;
  }
  .x3_time {
    font: 12px/36px "微软雅黑";
    color: #b4b4b4;
  }
  .x3_sm {
    font: 12px/18px "微软雅黑";
    color: #666666;
  }
  .clear {
    clear: both;
  }
  .right li {
    height: 100px;
    padding: 11px 55px 0 40px;
    background: #fcfcfc;
    margin-bottom: 1px;
  }
  .right li:hover {
    background: #197c56;
    .x3_sm,
    .x3_time,
    .x3_bt,
    .num {
      color: #fff;
      opacity: 1;
    }
  }
}
.hyzx {
  width: 100%;
  height: auto;
  padding-top: 50px;
  background: url(../../assets/img/hyzx.jpg) no-repeat center;
  background-attachment: fixed;
}
.flfg {
  background: url(../../assets/img/flfg.jpg) no-repeat center;
  background-attachment: fixed;
}
.join {
  background: url(../../assets/img/join.jpg) no-repeat center;
  background-attachment: fixed;
  .bod {
    .bt {
      font: 18px/18px "微软雅黑";
      color: #333333;
    }
    .bt:hover {
      color: #197c56;
    }
    .sm {
      padding: 30px 0;
    }
    .sm_p {
      font: 14px/30px "微软雅黑";
      color: #666666;
    }
    li {
      padding-left: 30px;
      background: url(../../assets/img/ind_06.png) no-repeat 0 8px;
    }
  }
}
.ind_box4 {
  padding-top: 115px;
  .li_img {
    padding-right: 20px;
  }
  .wz {
    float: right;
    width: 840px;
  }
  .new2 li {
    padding-bottom: 31px;
    border-bottom: 1px solid #e4e4e4;
    margin-bottom: 31px;
    height: 150px;
    .bt {
      color: rgb(51, 51, 51);
      padding-bottom: 5px;
      font: 14px/34px 微软雅黑;
    }
    .bt:hover {
      color: #197c56;
    }
    .sm {
      color: rgb(102, 102, 102);
      font: 12px/18px 微软雅黑;
    }
    .time {
      color: #a4a4a4;
      font: 12px/12px "Arial";
      padding-top: 10px;
    }
    .more {
      color: rgb(102, 102, 102);
      font: 12px/12px 微软雅黑;
    }
  }
}
.ind_box5 {
  padding-top: 115px;
}
.joi_box {
  padding: 28px 0 0 95px;
  width: 1005px;
  height: 272px;
  border: 1px solid #e7e7e7;
}
.slide-fade-enter-active {
  transition: all 1s ease;
}
.slide-fade-leave-active {
  transition: all 1s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active for below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
.pp {
  padding: 10px;
  cursor: pointer;
  font: 11px/36px "Arial";
  color: #fff;
  letter-spacing: 0.5px;
  filter: alpha(opacity=80);
  opacity: 0.8;
}
.new_inner {
  margin-bottom: 75px;
  width: 100%;
  .news_h1 {
    font: 14px/14px "微软雅黑";
    color: #333333;
    text-align: center;
  }
  .news_h3 {
    font: 12px/38px "微软雅黑";
    color: #a4a4a4;
    text-align: center;
    padding-bottom: 6px;
    border-bottom: 1px solid #e4e4e4;
  }
  .newp {
    font: 12px/18px "微软雅黑";
    color: #666666;
  }
}
</style>

