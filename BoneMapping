

import bpy
from mathutils import Matrix
from math import radians

#---functionlity logic----------
def getChildren(myObject): 
    children = [] 
    for ob in bpy.data.objects: 
        if ob.parent == myObject: 
            children.append(ob) 
    return children 

#filter function
def contains(list, filter):
    for x in list:
        if filter==x["boneName"]:
            return True
    return False


#boneNamesList= [{"boneName":"def_c_noseArc",  "tracker":"FaceEmpty_4"}]
boneNamesList= [
{"boneName":"def_r_lipCorner_a", "tracker":"FaceEmpty_61"},
{"boneName":"def_r_lipCorner_b",  "tracker":"FaceEmpty_62"},
{"boneName":"def_r_lipCorner_sticky",  "tracker":"FaceEmpty_78"},
{"boneName":"def_r_lipLowerOuter_a",  "tracker":"FaceEmpty_96"},
{"boneName":"def_r_lipUpperOuter_a",  "tracker":"FaceEmpty_183"},
{"boneName":"def_r_lipLowerOuter_sticky",  "tracker":"FaceEmpty_95"},
{"boneName":"def_r_lipUpperOuter_sticky",  "tracker":"FaceEmpty_191"},
{"boneName":"def_r_lipUpperOuter_b",  "tracker":"FaceEmpty_74"},
{"boneName":"def_r_lipLowerOuter_b",  "tracker":"FaceEmpty_90"},
{"boneName":"def_r_lipUpperCenter_sticky",  "tracker":"FaceEmpty_42"},
{"boneName":"def_r_lipUpperCenter_b",  "tracker":"FaceEmpty_39"},
{"boneName":"def_r_lipLower_a",  "tracker":"FaceEmpty_180"},
{"boneName":"def_r_innerlipUpper_a",  "tracker":"FaceEmpty_73"},
{"boneName":"def_r_lipLower_sticky",  "tracker":"FaceEmpty_179"},
{"boneName":"def_r_innerlipUpper_sticky",  "tracker":"FaceEmpty_38"},
{"boneName":"def_r_innerlipUpper_b",  "tracker":"FaceEmpty_72"},
{"boneName":"def_r_lipLower_b",  "tracker":"FaceEmpty_85"},

{"boneName":"def_l_lipCorner_a",  "tracker":"FaceEmpty_291"},
{"boneName":"def_l_lipCorner_b",  "tracker":"FaceEmpty_292"},
{"boneName":"def_l_lipCorner_sticky",  "tracker":"FaceEmpty_375"},
{"boneName":"def_l_lipLowerOuter_a",  "tracker":"FaceEmpty_308"},
{"boneName":"def_l_lipUpperOuter_a",  "tracker":"FaceEmpty_408"},
{"boneName":"def_l_lipLowerOuter_sticky",  "tracker":"FaceEmpty_324"},
{"boneName":"def_l_lipUpperOuter_sticky",  "tracker":"FaceEmpty_415"},
{"boneName":"def_l_lipUpperOuter_b",  "tracker":"FaceEmpty_304"},
{"boneName":"def_l_lipLowerOuter_b",  "tracker":"FaceEmpty_320"},
{"boneName":"def_l_lipUpperCenter_sticky",  "tracker":"FaceEmpty_272"},
{"boneName":"def_l_lipUpperCenter_b",  "tracker":"FaceEmpty_269"},
{"boneName":"def_l_lipLower_a",  "tracker":"FaceEmpty_404"},
{"boneName":"def_l_innerlipUpper_a",  "tracker":"FaceEmpty_303"},
{"boneName":"def_l_lipLower_sticky",  "tracker":"FaceEmpty_403"},
{"boneName":"def_l_innerlipUpper_sticky",  "tracker":"FaceEmpty_268"},
{"boneName":"def_l_innerlipUpper_b",  "tracker":"FaceEmpty_302"},
{"boneName":"def_l_lipLower_b",  "tracker":"FaceEmpty_315"},

#center section
{"boneName":"def_c_lipUpper_a",  "tracker":"FaceEmpty_11"},
{"boneName":"def_c_lipUpper_b",  "tracker":"FaceEmpty_11"},
{"boneName":"def_c_lipLower_a",  "tracker":"FaceEmpty_16"},
{"boneName":"def_c_lipLower_b",  "tracker":"FaceEmpty_16"},
{"boneName":"def_c_noseArc",  "tracker":"FaceEmpty_4"},
{"boneName":"def_c_noseMid",  "tracker":"FaceEmpty_195"},
{"boneName":"def_c_noseBridge",  "tracker":"FaceEmpty_168"},
{"boneName":"def_c_forehead",  "tracker":"FaceEmpty_9"},
{"boneName":"def_c_noseLower",  "tracker":"FaceEmpty_2"},
{"boneName":"def_c_chin",  "tracker":"FaceEmpty_175"},
{"boneName":"def_c_underChin",  "tracker":"FaceEmpty_152"},

{"boneName":"def_upperJaw",  "tracker":"FaceEmpty_11"},
{"boneName":"def_lowerJaw",  "tracker":"FaceEmpty_16"},
{"boneName":"def_c_teethTop",  "tracker":"FaceEmpty_11"},
{"boneName":"def_c_teethBot_manual",  "tracker":"FaceEmpty_16"},


#check section
{"boneName":"def_r_nasolabiaEdge",  "tracker":"FaceEmpty_216"},
{"boneName":"def_r_cheekLower",  "tracker":"FaceEmpty_192"},
{"boneName":"def_r_masseter",  "tracker":"FaceEmpty_137"},
{"boneName":"def_r_nasolabialBulge",  "tracker":"FaceEmpty_36"},
{"boneName":"def_r_nasolabialFurrow",  "tracker":"FaceEmpty_203"},
{"boneName":"def_r_cheekOuter",  "tracker":"FaceEmpty_117"},
{"boneName":"def_r_cheekInner",  "tracker":"FaceEmpty_47"},
{"boneName":"def_r_nostril",  "tracker":"FaceEmpty_115"},
{"boneName":"def_r_chinSide",  "tracker":"FaceEmpty_169"},
{"boneName":"def_r_underChin",  "tracker":"FaceEmpty_140"},
{"boneName":"def_r_foreheadIn",  "tracker":"FaceEmpty_55"},
{"boneName":"def_r_foreheadMid",  "tracker":"FaceEmpty_52"},
{"boneName":"def_r_foreheadOut",  "tracker":"FaceEmpty_46"},

{"boneName":"def_l_nasolabiaEdge",  "tracker":"FaceEmpty_436"},
{"boneName":"def_l_cheekLower",  "tracker":"FaceEmpty_416"},
{"boneName":"def_l_masseter",  "tracker":"FaceEmpty_366"},
{"boneName":"def_l_nasolabialBulge",  "tracker":"FaceEmpty_266"},
{"boneName":"def_l_nasolabialFurrow",  "tracker":"FaceEmpty_423"},
{"boneName":"def_l_cheekOuter",  "tracker":"FaceEmpty_346"},
{"boneName":"def_l_cheekInner",  "tracker":"FaceEmpty_277"},
{"boneName":"def_l_nostril",  "tracker":"FaceEmpty_344"},
{"boneName":"def_l_chinSide",  "tracker":"FaceEmpty_394"},
{"boneName":"def_l_underChin",  "tracker":"FaceEmpty_369"},
{"boneName":"def_l_foreheadIn",  "tracker":"FaceEmpty_285"},
{"boneName":"def_l_foreheadMid",  "tracker":"FaceEmpty_295"},
{"boneName":"def_l_foreheadOut",  "tracker":"FaceEmpty_276"},

#eye section
{"boneName":"def_r_eyesackLower",  "tracker":"FaceEmpty_230"},
{"boneName":"def_r_eyelidLower",  "tracker":"FaceEmpty_145"},
{"boneName":"def_r_eyelidLowerInner",  "tracker":"FaceEmpty_154"},
{"boneName":"def_r_eyelidUpperInner",  "tracker":"FaceEmpty_157"},
{"boneName":"def_r_eyesackUpper",  "tracker":"FaceEmpty_223"},
{"boneName":"def_r_eyelidUpper",  "tracker":"FaceEmpty_159"},
{"boneName":"def_r_eyelidUpperFurrow",  "tracker":"FaceEmpty_27"},
{"boneName":"def_r_eyelidUpperOutter",  "tracker":"FaceEmpty_161"},
{"boneName":"def_r_eyelidLowerOutter",  "tracker":"FaceEmpty_163"},

{"boneName":"def_l_eyesackLower",  "tracker":"FaceEmpty_450"},
{"boneName":"def_l_eyelidLower",  "tracker":"FaceEmpty_374"},
{"boneName":"def_l_eyelidLowerInner",  "tracker":"FaceEmpty_390"},
{"boneName":"def_l_eyelidUpperInner",  "tracker":"FaceEmpty_388"},
{"boneName":"def_l_eyesackUpper",  "tracker":"FaceEmpty_443"},
{"boneName":"def_l_eyelidUpper",  "tracker":"FaceEmpty_386"},
{"boneName":"def_l_eyelidUpperFurrow",  "tracker":"FaceEmpty_257"},
{"boneName":"def_l_eyelidUpperOutter",  "tracker":"FaceEmpty_388"},
{"boneName":"def_l_eyelidLowerOutter",  "tracker":"FaceEmpty_390"},

#miscellaneous - Fuse Model apex legends
#{"boneName":"def_c_moustache",  "tracker":"FaceEmpty_11"},
#{"boneName":"def_r_moustacheTop",  "tracker":"FaceEmpty_37"},
#{"boneName":"def_r_moustacheCorner",  "tracker":"FaceEmpty_185"},
#{"boneName":"def_r_moustacheOuter",  "tracker":"FaceEmpty_57"},
#{"boneName":"def_l_moustacheTop",  "tracker":"FaceEmpty_267"},
#{"boneName":"def_l_moustacheCorner",  "tracker":"FaceEmpty_409"},
#{"boneName":"def_l_moustacheOuter",  "tracker":"FaceEmpty_287"}

]

children = getChildren(bpy.data.collections['Face'].objects[0]) 
# make armature model be active
bpy.context.view_layer.objects.active = bpy.data.objects['root_Mirage.003']
armature=bpy.data.objects['root_Mirage.003']

#Enter Edit mode and make sure the bones head and tail x and y are the same. if not make it !
HeadAndTailDiff = False
if(bpy.context.active_object.mode != "EDIT_ARMATURE"):
   bpy.ops.object.editmode_toggle()
for poseBone in bpy.context.active_object.data.edit_bones:
   trackerName= [x['tracker'] for x in boneNamesList if x['boneName'] == poseBone.name]
   if len(trackerName)>0:
#        poseBone.roll=radians(0)
       if(poseBone.head.y != poseBone.tail.y):
           HeadAndTailDiff=True
           poseBone.tail.y= poseBone.head.y
           
            
#update the scene to get the updated value if there was a head and tail that was not the same
bpy.context.view_layer.update()

#Enter Pose mode.
if(bpy.context.active_object.mode != "POSE"):
    bpy.ops.object.posemode_toggle()
    
globalLocOriginal=0 #Original Vector of bones before the contraint is added
# loop through armature bones
for poseBone in bpy.context.active_object.pose.bones:
    trackerName= [x['tracker'] for x in boneNamesList if x['boneName'] == poseBone.name]
    if len(trackerName)>0:
        global_location = armature.matrix_world @ poseBone.matrix @ poseBone.location
        globalLocOriginal=global_location
        if len([x for x in  poseBone.constraints if x.name == "Copy Location"])==0:
            poseBone.constraints.new(type='COPY_LOCATION')
            for emptyTracker in children:
                if emptyTracker.name == trackerName[0]:
                    poseBone.constraints[0].target = emptyTracker
                    poseBone.constraints[0].use_offset=True
                    #update the scene to get the updated value
                    bpy.context.view_layer.update()
                    global_location = armature.matrix_world @ poseBone.matrix @ poseBone.location
                    poseBone.location.x = (globalLocOriginal.x - global_location.x )
                    poseBone.location.y = (globalLocOriginal.z - global_location.z )
                    poseBone.location.z = (globalLocOriginal.y - global_location.y )*-1
              
                    

#update the scene to get the updated value
bpy.context.view_layer.update()
 

## Remove bone Constraint
#bpy.context.view_layer.objects.active = bpy.data.objects['root_Mirage.003']
#armature=bpy.data.objects['root_Mirage.003']
##Enter Pose mode.
#for poseBone in bpy.context.active_object.pose.bones:
#    copyLocConstraints = [ c for c in poseBone.constraints if c.type == 'COPY_LOCATION' ]
#    for c in copyLocConstraints:
#        poseBone.constraints.remove( c ) # Remove constraint
#    poseBone.location.x = 0 
#    poseBone.location.y = 0 
#    poseBone.location.z = 0 
#    
    
    
## selecting a bone with a name containing 'Bone'
#bpy.context.view_layer.objects.active = bpy.data.objects['root_Lifeline.001']
#armature=bpy.data.objects['root_Lifeline.001']
##Enter Pose mode.
#for poseBone in bpy.context.active_object.pose.bones:
#    if "Bone" in poseBone.name:
#        poseBone.bone.select =True



for poseBone in bpy.context.active_object.pose.bones:
    if len([x for x in  poseBone.constraints if x.name == "Copy Location"])==1:
        poseBone.bone.select =True
